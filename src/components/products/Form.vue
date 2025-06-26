<script setup>
import { ref, watch, toRefs } from 'vue'

const props = defineProps({
  formData: {
    type: Object,
    default: () => ({ name: '', description: '', price: null, image: '' }),
  },
  isEditing: {
    type: Boolean,
    default: false,
  },
})

const emit = defineEmits(['save', 'cancel'])

const { formData } = toRefs(props)

const name = ref(formData.value.name)
const description = ref(formData.value.description)
const price = ref(formData.value.price)
const image = ref(formData.value.image)

watch(
  formData,
  (newVal) => {
    name.value = newVal.name || ''
    description.value = newVal.description || ''
    price.value = newVal.price || null
    image.value = newVal.image || ''
  },
  { immediate: true }
)

const submitForm = () => {
  if (!name.value || !price.value) {
    alert('Please fill in the name and price.')
    return
  }
  emit('save', {
    name: name.value,
    description: description.value,
    price: parseFloat(price.value),
    image: image.value || '/images/default.jpg',
  })
}

const cancel = () => {
  emit('cancel')
}
</script>

<template>
  <form @submit.prevent="submitForm" class="space-y-4">
    <h2 class="text-xl font-bold">{{ isEditing ? 'Edit Product' : 'Add New Product' }}</h2>
    <input
      v-model="name"
      type="text"
      placeholder="Product Name"
      class="w-full p-2 border rounded"
      required
    />
    <textarea
      v-model="description"
      placeholder="Description"
      class="w-full p-2 border rounded"
    ></textarea>
    <input
      v-model.number="price"
      type="number"
      step="0.01"
      placeholder="Price"
      class="w-full p-2 border rounded"
      required
    />
    <input
      v-model="image"
      type="text"
      placeholder="Image URL"
      class="w-full p-2 border rounded"
    />
    <div class="flex justify-end space-x-2">
      <button type="button" @click="cancel" class="px-4 py-2 border rounded">
        Cancel
      </button>
      <button type="submit" class="px-4 py-2 bg-green-500 text-white rounded">
        {{ isEditing ? 'Save Changes' : 'Add Product' }}
      </button>
    </div>
  </form>
</template>