<template>
  <div>
    <UButton variant="outline" @click="isOpen = true">Info</UButton>
    <UModal v-model="isOpen">
      <div class="p-4">
        <!-- <ContentDoc path="/info" /> -->
        <InfoModalContent />
      </div>
    </UModal>
  </div>
</template>

<script setup>
import InfoModalContent from "./InfoModalContent.vue";
const isOpen = ref(false);
</script>

<style lang="scss" scoped></style>
