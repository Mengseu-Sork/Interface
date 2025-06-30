<script setup>
import { ref } from 'vue';

const isOpen = ref(false);

const toggleMenu = () => {
  isOpen.value = !isOpen.value;
};
</script>

<template>
  <nav class="bg-green-600 shadow-md">
    <div class="container mx-auto px-4 py-4 flex items-center justify-between">
      <!-- Logo -->
      <div class="text-white text-2xl font-bold">Fruit Shop</div>

      <!-- Hamburger Icon (Mobile) -->
      <button
        @click="toggleMenu"
        class="text-white md:hidden focus:outline-none"
        aria-label="Toggle Menu"
      >
        <svg
          v-if="!isOpen"
          xmlns="http://www.w3.org/2000/svg"
          class="h-6 w-6"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
            d="M4 6h16M4 12h16M4 18h16" />
        </svg>
        <svg
          v-else
          xmlns="http://www.w3.org/2000/svg"
          class="h-6 w-6"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
            d="M6 18L18 6M6 6l12 12" />
        </svg>
      </button>

      <!-- Menu (Desktop) -->
      <ul class="hidden md:flex space-x-6 items-center">
        <li>
          <router-link
            to="/"
            class="text-white hover:text-yellow-300 transition-colors"
            active-class="text-yellow-300 font-semibold"
          >
            Home
          </router-link>
        </li>
        <li>
          <router-link
            to="/product"
            class="text-white hover:text-yellow-300 transition-colors"
            active-class="text-yellow-300 font-semibold"
          >
            Products
          </router-link>
        </li>
        <li>
          <router-link
            to="/about"
            class="text-white hover:text-yellow-300 transition-colors"
            active-class="text-yellow-300 font-semibold"
          >
            About Us
          </router-link>
        </li>
        <li>
          <router-link
            to="/contact"
            class="text-white hover:text-yellow-300 transition-colors"
            active-class="text-yellow-300 font-semibold"
          >
            Contact
          </router-link>
        </li>
        <li>
          <router-link to="" class="text-white hover:text-yellow-300">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-6 w-6"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
              stroke-width="2"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-1.5 6h11L17 13M9 21h.01M15 21h.01"
              />
            </svg>
          </router-link>
        </li>
      </ul>
    </div>

    <!-- Mobile Menu -->
    <div v-if="isOpen" class="md:hidden px-4 pb-4 space-y-2">
      <router-link
        to="/"
        class="block text-white hover:text-yellow-300"
        @click="toggleMenu"
        active-class="text-yellow-300 font-semibold"
      >
        Home
      </router-link>
      <router-link
        to="/product"
        class="block text-white hover:text-yellow-300"
        @click="toggleMenu"
        active-class="text-yellow-300 font-semibold"
      >
        Products
      </router-link>
      <router-link
        to="/about"
        class="block text-white hover:text-yellow-300"
        @click="toggleMenu"
        active-class="text-yellow-300 font-semibold"
      >
        About Us
      </router-link>
      <router-link
        to="/contact"
        class="block text-white hover:text-yellow-300"
        @click="toggleMenu"
        active-class="text-yellow-300 font-semibold"
      >
        Contact
      </router-link>
      <router-link
        to=""
        class="block text-white hover:text-yellow-300"
        @click="toggleMenu"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-6 w-6 inline"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
          stroke-width="2"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-1.5 6h11L17 13M9 21h.01M15 21h.01"
          />
        </svg>
      </router-link>
    </div>
  </nav>
</template>
