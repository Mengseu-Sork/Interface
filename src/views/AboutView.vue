<template>
  <div class="min-h-screen bg-green-50">
    <!-- Hero Section -->
    <section
      class="bg-cover bg-center"
      :style="`background-image: url('${heroImage}')`"
    >
      <div class="bg-gray-300 bg-opacity-60 py-32 px-4 text-center">
        <h1 class="text-4xl md:text-5xl font-bold text-green-600 mb-6">{{ heroTitle }}</h1>
        <router-link
          to="/product"
          class="inline-block bg-green-500 hover:bg-green-600 text-white font-semibold py-2 px-6 rounded-full transition"
        >
          Order Products
        </router-link>
      </div>
    </section>

    <!-- Content Section -->
    <section class="bg-white py-16 px-4 md:px-10 lg:px-20 rounded-lg shadow-lg mx-auto max-w-7xl -mt-12 z-10 relative">
      <div class="text-center">
        <h2 class="text-4xl font-bold text-green-700 mb-6">Our Mission</h2>
        <p class="text-lg text-gray-700 mb-12 max-w-3xl mx-auto">
          {{ missionText }}
        </p>

        <h2 class="text-4xl font-bold text-green-700 mb-6">Our Values</h2>
      </div>

      <div class="grid gap-8 md:grid-cols-3 mt-10">
        <div
          v-for="(value, index) in values"
          :key="index"
          class="bg-white rounded-xl shadow-md p-6 hover:shadow-xl transition duration-300"
        >
          <h3 class="text-xl font-semibold text-green-600 mb-2">{{ value.title }}</h3>
          <p class="text-gray-600">{{ value.description }}</p>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
const heroTitle = 'About Page'

const heroImage = 'https://i.pinimg.com/736x/da/a6/af/daa6af191ec4d8375a249e81a9d3ed1d.jpg'

const missionText = `At FreshFruit Market, our mission is to deliver the freshest, healthiest,
and most delicious fruits directly from farm to table. We believe in supporting
local farmers, promoting sustainable agriculture, and making nutritious choices
accessible to every home.`

const values = [
  {
    title: 'Freshness First',
    description:
      'We prioritize quality and freshness in everything we deliver. Our fruits are carefully selected and delivered quickly to preserve taste and nutrients.',
  },
  {
    title: 'Sustainability',
    description:
      'We support eco-friendly farming and packaging practices to protect the planet while providing the best produce.',
  },
  {
    title: 'Customer Care',
    description:
      'Your satisfaction is our priority. From easy ordering to fast delivery, we strive to make your fruit shopping simple and enjoyable.',
  },
]
</script>
