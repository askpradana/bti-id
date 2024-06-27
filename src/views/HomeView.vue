<script setup>
import SingleWidget from '@/components/SingleWidget.vue'
import ModalDialog from '@/components/ModalDialog.vue'
import DialogContent from '@/components/DialogContent.vue'

const jobDesc = [
  'Monitor competition to identify new industry trends and opportunities for innovation',
  'Monitor competition to identify new industry trends and opportunities for innovation',
  'Monitor competition to identify new industry trends and opportunities for innovation',
  'Monitor competition to identify new industry trends and opportunities for innovation',
  'Monitor competition to identify new industry trends and opportunities for innovation',
  'Monitor competition to identify new industry trends and opportunities for innovation'
]
const skillDesc = ['Java', 'Spring boot', 'Vue', 'Vite', 'Tailwind', 'Nuxt']
const titleList = [
  'Marketing Planner',
  'UI/UX Content planner',
  'HR/Legal manager',
  'UI/UX Content writer',
  'UI/UX Designer',
  'Java spring boot'
]
</script>

<template>
  <main class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
    <div v-for="i in titleList.length" :key="i - 1">
      <SingleWidget :title="titleList[i - 1]">
        <ModalDialog :title="titleList[i - 1]">
          <DialogContent :listOfString="jobDesc" :listOfSkill="skillDesc" />
        </ModalDialog>
      </SingleWidget>
    </div>
  </main>
</template>
