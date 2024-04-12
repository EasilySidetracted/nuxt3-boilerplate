<template>
  <div>
    <header>
      <ClientOnly fallbackTag="div">
        <UButtonGroup orientation="horizontal">
          <HeaderThemeSwitch />
          <HeaderInfoModal />
        </UButtonGroup>
        <template #fallback>
          <div class="w-8 h-8" />
          <div class="w-8 h-8" />
        </template>
      </ClientOnly>
    </header>
  </div>
</template>

<script setup lang="ts">
import HeaderInfoModal from "./HeaderInfoModal.vue";
import HeaderThemeSwitch from "./HeaderThemeSwitch.vue";
</script>

<style scoped>
header {
  float: right;
  margin-bottom: 1rem;
}
</style>
