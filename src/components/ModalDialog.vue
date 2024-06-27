<script setup>
defineProps({
  title: String
})
</script>

<template>
  <div class="text-center">
    <v-dialog max-width="800">
      <template v-slot:activator="{ props: activatorProps }">
        <v-btn
          v-bind="activatorProps"
          text="See Job"
          color="orange-lighten-2"
          elevation="0"
        ></v-btn>
      </template>

      <template v-slot:default="{ isActive }">
        <v-card :title="title" class="pl-6 py-4">
          <slot />

          <v-card-actions>
            <!-- <v-btn text="Disagree" variant="text" @click="isActive.value = false"></v-btn> -->

            <v-btn text="Send Message" variant="tonal" @click="isActive.value = false"></v-btn>
            <v-spacer></v-spacer>
          </v-card-actions>
        </v-card>
      </template>
    </v-dialog>
  </div>
</template>
