<template>
  <footer class="bg-green-700 text-white py-8">
    <div class="container mx-auto px-4">
      <div class="flex flex-col md:flex-row justify-between gap-8 flex-wrap max-w-6xl mx-auto">
        <!-- About Section -->
        <div class="flex-1 min-w-[250px]">
          <h2 class="text-xl text-center font-semibold mb-2">{{ appName }}</h2>
          <p class="text-sm ml-4 leading-relaxed">
            {{ aboutText }}
          </p>
        </div>

        <!-- Quick Links -->
        <div class="flex-1 text-center min-w-[250px]">
          <h2 class="text-xl font-semibold mb-2">Quick Links</h2>
          <ul class="space-y-2 text-sm">
            <li v-for="link in quickLinks" :key="link.name">
              <router-link :to="link.to" class="hover:text-yellow-300 transition">
                {{ link.name }}
              </router-link>
            </li>
          </ul>
        </div>

        <!-- Contact Info -->
        <div class="flex-1 min-w-[250px]">
          <h2 class="text-xl text-center font-semibold mb-2">Contact</h2>
          <ul class="space-y-2 ml-12 text-sm">
            <li><span class="font-medium">Email:</span> {{ contact.email }}</li>
            <li><span class="font-medium">Phone:</span> {{ contact.phone }}</li>
            <li><span class="font-medium">Location:</span> {{ contact.location }}</li>
          </ul>
        </div>
      </div>

      <!-- Bottom Bar -->
      <div class="mt-8 pt-4 border-t border-green-500 text-center text-sm text-gray-200">
        © 2025 {{ appName }}. All rights reserved.
      </div>
    </div>
  </footer>
</template>

<script setup>
const appName = 'Fruit Shop'

const aboutText =
  'We offer the freshest fruits delivered to your door. Grown organically and sourced locally.'

const quickLinks = [
  { name: 'Home', to: '/' },
  { name: 'Fruits', to: '/fruits' },
  { name: 'About Us', to: '/about' },
  { name: 'Contact', to: '/contact' }
]

const contact = {
  email: 'mengseu.sork212004@gmail.com',
  phone: '+855 86 788 826',
  location: 'Phnom Penh, Cambodia'
}
</script>
