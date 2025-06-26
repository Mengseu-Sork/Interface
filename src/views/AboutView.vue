<template>
  <div class="min-h-screen bg-green-50 py-6 px-6">
    <div class="container mx-auto max-w-full bg-white rounded-lg shadow-lg p-10">
      <h1 class="text-4xl font-bold text-green-800 mb-8 text-center">About Our Products</h1>

      <p class="text-gray-700 text-lg mb-6 leading-relaxed">
        At Fruit Shop, we pride ourselves on offering a wide variety of fresh, organic fruits sourced from trusted local farms.
        Our products are carefully selected to ensure the highest quality and delicious taste in every bite.
      </p>

      <h2 class="text-2xl font-semibold text-green-700 mb-4">Why Choose Our Fruits?</h2>
      <ul class="list-disc list-inside mb-6 text-gray-700 space-y-2">
        <li>100% Organic and pesticide-free fruits for your health.</li>
        <li>Locally sourced to support sustainable farming practices.</li>
        <li>Handpicked fresh to guarantee peak ripeness and flavor.</li>
        <li>Wide selection including apples, bananas, mangoes, oranges, and more.</li>
        <li>Delivered directly to your door for ultimate convenience.</li>
      </ul>

      <h2 class="text-2xl font-semibold text-green-700 mb-4">Our Commitment to Quality</h2>
      <p class="text-gray-700 text-lg leading-relaxed">
        We work closely with farmers to ensure that every fruit meets strict quality standards.
        From farm to table, our fruits maintain their freshness and nutritional value.
        We believe that healthy eating starts with the best ingredients.
      </p>

      <div class="mt-10 text-center">
        <router-link
          to="/product"
          class="inline-block bg-green-700 text-white py-3 px-8 rounded-full font-semibold hover:bg-green-800 transition"
        >
          Browse Our Products
        </router-link>
      </div>
    </div>
  </div>
</template>
