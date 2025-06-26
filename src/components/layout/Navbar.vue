<template>
  <nav class="bg-green-600 p-4 shadow-md">
    <div class="container mx-auto flex items-center justify-between">

      <div class="flex items-center space-x-2">
        <span class="text-white ml-8 text-2xl font-bold">Fruit Shop</span>
      </div>


      <ul class="flex space-x-6 items-center">
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
  </nav>
</template>
