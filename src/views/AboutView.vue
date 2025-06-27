<template>
  <div class="min-h-screen bg-green-50">
    <section
        class="bg-cover bg-center"
        style="background-image: url('https://i.pinimg.com/736x/da/a6/af/daa6af191ec4d8375a249e81a9d3ed1d.jpg');"
      >
        <div class="bg-gray-300 bg-opacity-60 py-32 px-2 max-w-8xl mx-auto text-center">
          <h1 class="text-4xl font-bold text-green-500 mb-8">About Page</h1>
          <router-link
            to="/product"
            class="bg-green-400 hover:bg-green-500 text-white font-semibold py-2 px-6 rounded-full transition"
          >
            Order Products
          </router-link>
        </div>
    </section>
    
    <div class="container mx-auto max-w-full bg-white rounded-lg shadow-lg p-10">
      <section class="bg-gradient-to-b from-green-50 to-white py-12 px-6 md:px-20">
        <div class="max-w-5xl mx-auto text-center">
          <h2 class="text-4xl font-bold text-green-700 mb-4">Our Mission</h2>
          <p class="text-lg text-gray-700 mb-10">
            At <span class="font-semibold text-green-600">FreshFruit Market</span>, our mission is to deliver the freshest, healthiest, and most delicious fruits directly from farm to table. We believe in supporting local farmers, promoting sustainable agriculture, and making nutritious choices accessible to every home.
          </p>

          <h2 class="text-4xl font-bold text-green-700 mb-4">Our Values</h2>
          <div class="grid md:grid-cols-3 gap-8 text-left mt-6">
            <div class="bg-white rounded-xl shadow-md p-6 hover:shadow-xl transition-shadow duration-300 ease-in-out">
              <h3 class="text-xl font-semibold text-green-600 mb-2">Freshness First</h3>
              <p class="text-gray-600">
                We prioritize quality and freshness in everything we deliver. Our fruits are carefully selected and delivered quickly to preserve taste and nutrients.
              </p>
            </div>
            <div class="bg-white rounded-xl shadow-md p-6 hover:shadow-xl transition-shadow duration-300 ease-in-out">
              <h3 class="text-xl font-semibold text-green-600 mb-2">Sustainability</h3>
              <p class="text-gray-600">
                We support eco-friendly farming and packaging practices to protect the planet while providing the best produce.
              </p>
            </div>
            <div class="bg-white rounded-xl shadow-md p-6 hover:shadow-xl transition-shadow duration-300 ease-in-out">
              <h3 class="text-xl font-semibold text-green-600 mb-2">Customer Care</h3>
              <p class="text-gray-600">
                Your satisfaction is our priority. From easy ordering to fast delivery, we strive to make your fruit shopping simple and enjoyable.
              </p>
            </div>
          </div>
        </div>
      </section>

    </div>
  </div>
</template>
