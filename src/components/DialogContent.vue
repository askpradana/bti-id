<script setup>
import { Upload } from 'lucide-vue-next'
defineProps({
  title: String,
  listOfString: Array,
  skill: String,
  listOfSkill: Array
})
</script>
<template>
  <main class="px-6">
    <h2 class="text-xl font-semibold">{{ title }}:</h2>
    <ul class="pl-12">
      <li v-for="item in listOfString" :key="item" class="list-disc">{{ item }}</li>
    </ul>

    <h2 class="text-xl font-semibold pt-4">{{ skill }}:</h2>
    <ul class="pl-12">
      <li v-for="item in listOfSkill" :key="item" class="list-disc">{{ item }}</li>
    </ul>

    <h2 class="text-xl font-semibold pt-8 pb-4">Send your job application</h2>

    <div class="flex flex-row w-full">
      <div class="flex flex-col w-full mr-6">
        <div class="flex flex-col w-full border-b-2">
          <label for="name" class="font-semibold pb-2">Your Name</label>
          <input type="text" name="name" id="name" placeholder="Enter your name" />
        </div>
        <div class="flex flex-col w-full border-b-2 pt-4">
          <label for="email" class="font-semibold pb-2">Email Address</label>
          <input type="email" name="email" id="email" placeholder="Enter your email address" />
        </div>
      </div>

      <div class="flex flex-col w-full">
        <div class="flex flex-col w-full border-b-2">
          <label for="name" class="font-semibold pb-2">Mobile Number</label>
          <input type="text" name="name" id="name" placeholder="Enter your mobile number " />
        </div>
        <div class="flex flex-col w-full border-b-2 pt-4">
          <label for="email" class="font-semibold pb-2">Write Your message here...</label>
          <input type="email" name="email" id="email" placeholder="Write your message" />
        </div>
      </div>
    </div>

    <div class="pb-12">
      <h2 class="font-semibold text-xl pt-8 pb-4">File</h2>
      <div
        class="bg-orange-500 w-[80px] h-[80px] flex justify-center items-center cursor-pointer rounded-lg"
      >
        <label for="upload-file" class="cursor-pointer">
          <Upload />
        </label>
        <input type="file" id="upload-file" name="upload-file" class="opacity-0 absolute -z-10" />
      </div>
    </div>
  </main>
</template>
