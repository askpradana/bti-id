<script setup>
import { ref } from 'vue'

defineProps({
  title: String
})

let dialogState = ref(false)

function toggleDialog() {
  dialogState.value = !dialogState.value
}
</script>

<template>
  <main>
    <div class="bg-stone-200 px-4 py-2 rounded-lg shadow-md shadow-stone-400 m-4">
      <div class="py-2 flex flex-row justify-between items-center w-full">
        <h1 class="font-semibold text-green-600">{{ title }}</h1>
        <button class="bg-orange-500 text-white font-bold py-1 px-4 rounded" @click="toggleDialog">
          <p>See job</p>
        </button>
      </div>
    </div>
    <dialog :open="dialogState" class="backdrop:bg-gray-500">
      <slot />
    </dialog>
  </main>
</template>
