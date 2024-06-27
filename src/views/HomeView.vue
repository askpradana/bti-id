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
  <main>
    <SingleWidget :title="titleList[0]">
      <ModalDialog :title="titleList[0]">
        <DialogContent
          title="Job Description"
          :listOfString="jobDesc"
          :skill="titleList[0]"
          :listOfSkill="skillDesc"
        />
      </ModalDialog>
    </SingleWidget>
  </main>
</template>
