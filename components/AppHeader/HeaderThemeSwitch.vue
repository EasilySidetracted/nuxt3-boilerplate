<template>
  <div>
    <UButton
      :icon="isDark ? 'i-heroicons-moon-20-solid' : 'i-heroicons-sun-20-solid'"
      color="primary"
      variant="outline"
      aria-label="Theme"
      @click="isDark = !isDark"
    />
  </div>
</template>

<script setup>
const colorMode = useColorMode();
const isDark = computed({
  get() {
    return colorMode.value === "dark";
  },
  set() {
    colorMode.preference = colorMode.value === "dark" ? "light" : "dark";
  },
});
</script>

<style lang="scss" scoped></style>
