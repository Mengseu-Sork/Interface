<script setup>
const props = defineProps({
  product: {
    type: Object,
    required: true,
  },
})
const emit = defineEmits(['buy'])
</script>

<template>
  <div
    class="bg-white rounded-xl shadow-md hover:shadow-2xl transition-shadow duration-300 ease-in-out overflow-hidden flex flex-col items-center w-[280px] h-[390px] pb-6"
  >
    <div class="w-full h-40 flex items-center justify-center p-4">
      <img
        :src="product.image"
        alt="Product"
        class="max-w-full max-h-full object-contain"
      />
    </div>

    <div class="flex-grow flex flex-col items-center px-4 text-center">
      <h3 class="text-xl font-semibold text-gray-800 mt-2">{{ product.name }}</h3>
      <p class="text-gray-600 text-sm mt-1 mb-2">{{ product.description }}</p>

      <span class="text-lg font-bold text-gray-800">${{ product.price.toFixed(2) }}</span>

      <div class="flex items-center mt-3 mb-4">
        <svg v-for="n in 4" :key="'filled-' + n" class="w-5 h-5 text-yellow-400 fill-current" viewBox="0 0 24 24">
          <path d="M12 .587l3.668 7.424 8.204 1.192-5.946 5.793 1.402 8.163L12 18.896l-7.328 3.854 1.402-8.163-5.946-5.793 8.204-1.192L12 .587z"/>
        </svg>
        <svg class="w-5 h-5 text-gray-300 fill-current" viewBox="0 0 24 24">
          <path d="M12 .587l3.668 7.424 8.204 1.192-5.946 5.793 1.402 8.163L12 18.896l-7.328 3.854 1.402-8.163-5.946-5.793 8.204-1.192L12 .587z"/>
        </svg>
      </div>
    </div>

    <Button
      class="w-4/5 py-3 rounded-lg text-white font-semibold transition-colors duration-200"
      @click="$emit('buy', product)"
      label="Buy Now"
      color="green"
    />
      
  </div>
</template>