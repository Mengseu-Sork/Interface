<template>
  <div
    class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50"
    @click.self="$emit('close')"
  >
    <div class="bg-white rounded-lg shadow-lg p-6 max-w-lg w-full">
      <button
        class="float-right text-gray-500 hover:text-gray-700"
        @click="$emit('close')"
        aria-label="Close"
      >
        &times;
      </button>
      <slot />
    </div>
  </div>
</template>

<script setup>
</script>
