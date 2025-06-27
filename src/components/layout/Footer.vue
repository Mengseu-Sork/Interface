<template>
  <footer class="bg-green-700 text-white py-8">
    <div class="container mx-auto px-4">
      <div class="flex flex-col md:flex-row justify-between flex-wrap gap-8 max-w-6xl mx-auto">
        <!-- About Section -->
        <div class="flex-1 mr-8 min-w-[250px]">
          <h2 class="text-xl font-semibold mb-2">Fruit Shop</h2>
          <p class="text-sm">
            We offer the freshest fruits delivered to your door. Grown organically and sourced locally.
          </p>
        </div>

        <!-- Quick Links -->
        <div class="flex-1 min-w-[250px] ml-12">
          <h2 class="text-xl font-semibold mb-2">Quick Links</h2>
          <ul class="space-y-2 text-sm">
            <li><router-link to="/" class="hover:text-yellow-300">Home</router-link></li>
            <li><router-link to="/fruits" class="hover:text-yellow-300">Fruits</router-link></li>
            <li><router-link to="/about" class="hover:text-yellow-300">About Us</router-link></li>
            <li><router-link to="/contact" class="hover:text-yellow-300">Contact</router-link></li>
          </ul>
        </div>

        <!-- Contact Info -->
        <div class="flex-1 min-w-[250px]">
          <h2 class="text-xl font-semibold mb-2">Contact</h2>
          <ul class="text-sm space-y-2">
            <li><span class="font-medium">Email:</span> mengseu.sork212004@gmail.com</li>
            <li><span class="font-medium">Phone:</span> +855 86 788 826</li>
            <li><span class="font-medium">Location:</span> Phnom Penh, Cambodia</li>
          </ul>
        </div>
      </div>

      <!-- Bottom Bar -->
      <div class="mt-8 text-center text-sm text-gray-200 border-t border-green-500 pt-4">
        © 2025 Fruit Shop. All rights reserved.
      </div>
    </div>
  </footer>
</template>
