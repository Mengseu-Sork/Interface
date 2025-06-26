<script setup>
import { ref, watch } from 'vue'
import Modal from '@/components/products/Modal.vue'
import ProductForm from '@/components/products/Form.vue'
import ProductCard from '@/components/products/Card.vue'

const products = ref(
  JSON.parse(localStorage.getItem('products')) || [
    {
      id: Date.now(),
      name: 'Fresh Mango',
      description: 'A tropical delight with smooth texture in every bite.',
      price: 2.49,
      image: 'https://i.pinimg.com/736x/68/e4/73/68e473002d030395640718bc5462eabb.jpg',
    },
    {
      id: Date.now(),
      name: 'Green Apple',
      description: 'Tart and crisp, green apples are ideal for a healthy snack or a tangy pie.',
      price: 1.99,
      image: 'https://i.pinimg.com/736x/df/87/69/df8769eeccb08aad302325f91996e2d0.jpg',
    },
    {
      id: Date.now(),
      name: 'Oranges',
      description: 'Bright, juicy oranges perfect for a healthy snack or fresh juice.',
      price: 1.99,
      image: 'https://i.pinimg.com/736x/7a/aa/a5/7aaaa545e00e8a434850e80b8910dd94.jpg',
    },
    {
      id: Date.now(),
      name: 'Banana',
      description: 'Naturally sweet and creamy, bananas are a perfect energy-boosting snack.',
      price: 1.99,
      image: 'https://i.pinimg.com/736x/02/49/5f/02495fb1b8bd32a24fb8eb483a18a074.jpg',
    },
  ]
)

const showForm = ref(false)
const isEditing = ref(false)
const formData = ref(null)

watch(products, (newProducts) => {
  localStorage.setItem('products', JSON.stringify(newProducts))
}, { deep: true })

const openCreateForm = () => {
  formData.value = { name: '', description: '', price: null, image: '' }
  isEditing.value = false
  showForm.value = true
}

const saveProduct = (product) => {
  if (isEditing.value) {
    const index = products.value.findIndex((p) => p.name === product.name)
    if (index !== -1) products.value[index] = product
  } else {
    products.value.push(product)
  }
  showForm.value = false
}

const cancelForm = () => {
  showForm.value = false
}

</script>

<template>
  <div class="bg-white">
    <section
      class="bg-cover bg-center"
      style="background-image: url('https://i.pinimg.com/736x/7a/aa/a5/7aaaa545e00e8a434850e80b8910dd94.jpg');"
    >
      <div
        class="bg-gray-300 bg-opacity-60 py-32 px-2 max-w-8xl mx-auto text-center"
      >
        <h1 class="text-4xl font-bold text-white mb-4">Products List</h1>
        <p class="text-lg text-white mb-6">
          Fresh. Organic. Delivered to your door.
        </p>
        <router-link
          to="#"
          class="bg-green-400 hover:bg-green-500 text-white font-semibold py-2 px-6 rounded-full transition"
        >
          Order Now
        </router-link>
      </div>
    </section>

    <section class="bg-gray-50 min-h-screen p-6 ml-2">
      <button
        @click="openCreateForm"
        class="mb-6 px-4 py-2 bg-green-500 text-white rounded"
      >
        Add New Product
      </button>

      <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-6">
        <ProductCard
          v-for="product in products"
          :key="product.name"
          :product="product"
        />
      </div>

      <Modal v-if="showForm" @close="cancelForm">
        <ProductForm
          :formData="formData"
          :isEditing="isEditing"
          @save="saveProduct"
          @cancel="cancelForm"
        />
      </Modal>
    </section>
  </div>
</template>