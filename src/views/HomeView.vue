<script setup>

const steps = [
  {
    title: 'Choose Fruits',
    icon: 'https://i.pinimg.com/736x/28/23/fd/2823fd196cf03582f1bd4a2109344f08.jpg',
    description: "Discover and select your favorite fruits from a wide variety of fresh, juicy, and nutritious options.",
  },
  {
    title: 'Address',
    icon: 'https://i.pinimg.com/736x/6d/a0/5a/6da05a452c869afed7c4ab06c8d5ead3.jpg',
    description: 'Find us at our main office location below. We welcome visits during working hours.',
  },
  {
    title: 'Delivery',
    icon: 'https://i.pinimg.com/736x/03/6c/cd/036ccd2c239246765b080b02b2f41ca1.jpg',
    description: 'We deliver fresh fruits quickly and safely to your doorstep — just place your order and we’ll handle the rest!',
  },
];
</script>

<template>
  <div class="bg-white">
    <section
      class="bg-cover bg-center"
      style="background-image: url('https://images.unsplash.com/photo-1567306226416-28f0efdc88ce');"
    >
      <div class="bg-gray-300 bg-opacity-60 py-32 px-2 max-w-8xl mx-auto text-center">
        <h1 class="text-4xl font-bold text-white mb-4">Welcome to Fruit Shop</h1>
        <p class="text-lg text-white mb-6">Fresh. Organic. Delivered to your door.</p>
        <router-link
          to="/product"
          class="bg-green-400 hover:bg-green-500 text-white font-semibold py-2 px-6 rounded-full transition"
        >
          Shop Now
        </router-link>
      </div>
    </section>

    <section class="py-8 px-6 bg-white">
      <div class="max-w-6xl mx-auto text-center">
        <h2 class="text-3xl font-bold text-gray-800 mb-4">Why Choose Our Fruits?</h2>
        <p class="text-gray-600 mb-10 max-w-3xl mx-auto">
          Our fruits are handpicked from the best farms and delivered fresh to your door.
          We prioritize organic and sustainable farming to ensure you get the healthiest produce.
        </p>

        <div class="grid grid-cols-1 md:grid-cols-3 gap-8 text-left">
          <div class="p-6 rounded-lg border hover:shadow-lg transition">
            <h3 class="text-xl font-semibold text-green-600 mb-2">100% Organic</h3>
            <p class="text-gray-600">No pesticides or chemicals used. Just clean, natural fruit the way nature intended.</p>
          </div>
          <div class="p-6 rounded-lg border hover:shadow-lg transition">
            <h3 class="text-xl font-semibold text-green-600 mb-2">Fresh & Local</h3>
            <p class="text-gray-600">We source locally from trusted farms to ensure freshness and support local communities.</p>
          </div>
          <div class="p-6 rounded-lg border hover:shadow-lg transition">
            <h3 class="text-xl font-semibold text-green-600 mb-2">Fast Delivery</h3>
            <p class="text-gray-600">Order today and get it delivered tomorrow – safe, fast, and convenient service every time.</p>
          </div>
        </div>
      </div>
    </section>

    <div class="bg-cover bg-center py-12 px-6">
      <h2 class="text-3xl font-bold text-gray-800 mb-4 text-center">Our Locations</h2>
      <div class="max-w-6xl mx-auto grid grid-cols-1 md:grid-cols-3 gap-8">
        <div
          v-for="step in steps"
          :key="step.title"
          class="bg-white rounded-3xl p-8 text-center border hover:shadow-lg duration-300"
        >
          <img :src="step.icon" alt="icon" class="h-32 w-32 mx-auto mb-4" />
          <h3 class="text-xl font-bold mb-2">{{ step.title }}</h3>
          <p class="text-gray-600 text-sm">{{ step.description }}</p>
        </div>
      </div>
    </div>
  </div>
</template>
