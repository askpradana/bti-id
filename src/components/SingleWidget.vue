<script setup>
defineProps({
  title: String
})
</script>

<template>
  <main class="bg-stone-200 px-4 py-2 rounded-lg shadow-md shadow-stone-400">
    <div class="py-2 flex flex-row justify-between items-center w-full">
      <h1 class="font-semibold text-green-600">{{ title }}</h1>
      <slot />
    </div>
  </main>
</template>
