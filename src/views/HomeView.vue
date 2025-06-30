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
const h1 = "Welcome to Fruit Shop"
const p1 = "Fresh. Organic. Delivered to your door."
const h2 = "Why Choose Our Fruits?"
const p2 = "Our fruits are handpicked from the best farms and delivered fresh to your door. We prioritize organic and sustainable farming to ensure you get the healthiest produce."
const p3 = "No pesticides or chemicals used. Just clean, natural fruit the way nature intended."
const p4 = "We source locally from trusted farms to ensure freshness and support local communities."
const p5 = "Order today and get it delivered tomorrow – safe, fast, and convenient service every time."

</script>

<template>
  <div class="bg-white">
    <main class="max-w-screen-xl mx-auto">

      <!-- Hero Section -->
      <header
        class="bg-cover bg-center"
        style="background-image: url('https://images.unsplash.com/photo-1567306226416-28f0efdc88ce');"
      >
        <div class="bg-gray-300 bg-opacity-60 py-24 px-4 sm:px-6 md:px-10 text-center">
          <h1 class="text-3xl sm:text-4xl font-bold text-white drop-shadow-md mb-4">
            {{ h1 }}
          </h1>
          <p class="text-base sm:text-lg text-white drop-shadow-sm mb-6">
            {{ p1 }}
          </p>
          <router-link
            to="/product"
            class="bg-green-400 hover:bg-green-500 text-white font-semibold py-2 px-6 rounded-full transition"
          >
            Shop Now
          </router-link>
        </div>
      </header>

      <!-- Features Section -->
      <section class="py-12 px-4 sm:px-6 md:px-8 lg:px-10">
        <div class="max-w-6xl mx-auto text-center">
          <h2 class="text-2xl sm:text-3xl font-bold text-gray-800 mb-4">{{ h2 }}</h2>
          <p class="text-gray-600 mb-10 max-w-3xl mx-auto">
            {{ p2 }}
          </p>

          <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6 text-left">
            <div class="p-6 rounded-lg border hover:shadow-lg transition">
              <h3 class="text-xl font-semibold text-green-600 mb-2">100% Organic</h3>
              <p class="text-gray-600">{{ p3 }}</p>
            </div>
            <div class="p-6 rounded-lg border hover:shadow-lg transition">
              <h3 class="text-xl font-semibold text-green-600 mb-2">Fresh & Local</h3>
              <p class="text-gray-600">{{ p4 }}</p>
            </div>
            <div class="p-6 rounded-lg border hover:shadow-lg transition">
              <h3 class="text-xl font-semibold text-green-600 mb-2">Fast Delivery</h3>
              <p class="text-gray-600">{{ p5 }}</p>
            </div>
          </div>
        </div>
      </section>

      <!-- Steps / Locations Section -->
      <section class="py-12 px-4 sm:px-6 md:px-10">
        <h2 class="text-2xl sm:text-3xl font-bold text-gray-800 mb-8 text-center">Our Locations</h2>
        <div class="max-w-6xl mx-auto grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-8">
          <div
            v-for="step in steps"
            :key="step.title"
            class="bg-white rounded-3xl p-6 sm:p-8 text-center border hover:shadow-lg duration-300"
          >
            <img
              :src="step.icon"
              alt="icon"
              class="w-24 h-24 sm:w-28 sm:h-28 md:w-32 md:h-32 object-cover rounded-full mx-auto mb-4 hover:scale-105 transition-transform duration-300"
            />
            <h3 class="text-lg sm:text-xl font-bold mb-2">{{ step.title }}</h3>
            <p class="text-gray-600 text-sm">{{ step.description }}</p>
          </div>
        </div>
      </section>

    </main>
  </div>
</template>
