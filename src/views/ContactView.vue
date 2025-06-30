<script setup>
const h2 = "Contact Us"
const h3 = "Get In Touch"
const p1 = "We’d love to hear from you! Reach out with questions, feedback, or just to say hello."
const p2 = "Have questions about our fruits, delivery, or business partnerships? Contact us any time!"
const contactInfo = [
  { label: 'Phone', icon: '📞', value: '+855 86 788 826' },
  { label: 'Email', icon: '📧', value: 'mengseu.sork212004@gmail.com' },
  { 
    label: 'Address', 
    icon: '', 
    value: '(Borey Sorla) Sangtak, Street 371, Phnom Penh', 
    imageUrl: 'https://cdn4.iconfinder.com/data/icons/travel-and-holiday-3/32/location-512.png',
    isAddress: true
  }
]
</script>
<template>
    <section class="bg-white py-12 px-6 md:px-20">
  <div class="max-w-6xl mx-auto">
    <div class="text-center mb-12">
      <h2 class="text-4xl font-bold text-green-700">{{ h2 }}</h2>
      <p class="text-gray-600 mt-2">{{ p1 }}</p>
    </div>

    <div class="grid md:grid-cols-2 gap-10">
      <div>
        <h3 class="text-2xl font-semibold text-green-600 mb-4">{{ h3 }}</h3>
        <p class="text-gray-700 mb-4">{{ p2 }}</p>
        <ul class="space-y-3 text-gray-700">
          <li v-for="(item, index) in contactInfo" :key="index" :class="item.isAddress ? 'flex items-center' : ''">
            <template v-if="item.isAddress">
              <img
                :src="item.imageUrl"
                alt="Location Icon"
                class="h-6 w-6 mr-1"
              />
              <strong class="mr-1">{{ item.label }}:</strong>{{ item.value }}
            </template>
            <template v-else>
              <strong>{{ item.icon }} {{ item.label }}:</strong> {{ item.value }}
            </template>
          </li>
        </ul>

        <div class="flex-1 mt-6">
            <iframe
                class="w-full h-[215px] rounded-lg shadow-lg"
                loading="lazy"
                allowfullscreen
                referrerpolicy="no-referrer-when-downgrade"
                src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d15641.775476529713!2d104.87228355!3d11.55086615!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x310951add5e2cd81%3A0x171e0b69c7c6f7ba!2sPasserelles%20num%C3%A9riques%20Cambodia%20(PNC)!5e0!3m2!1sen!2skh!4v1718700000000!5m2!1sen!2skh"
                />
        </div>

      </div>

      <form class="bg-green-50 p-6 rounded-xl shadow-md space-y-5">
        <div>
          <label class="block mb-1 text-sm font-medium text-green-800">Your Name</label>
          <input type="text" class="w-full px-4 py-2 border border-green-200 rounded-md focus:outline-none focus:ring-2 focus:ring-green-400" required />
        </div>
        <div>
          <label class="block mb-1 text-sm font-medium text-green-800">Your Email</label>
          <input type="email" class="w-full px-4 py-2 border border-green-200 rounded-md focus:outline-none focus:ring-2 focus:ring-green-400" required />
        </div>
        <div>
          <label class="block mb-1 text-sm font-medium text-green-800">Message</label>
          <textarea rows="5" class="w-full px-4 py-2 border border-green-200 rounded-md focus:outline-none focus:ring-2 focus:ring-green-400" required></textarea>
        </div>
        <button type="submit" class="w-full bg-green-600 text-white py-2 rounded-md hover:bg-green-700 transition duration-300">
          Send Message
        </button>
      </form>

    </div>
  </div>
</section>

</template>