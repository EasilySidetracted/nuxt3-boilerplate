<template>
  <div>
    <UDivider label="Divider" size="sm" />
    <UButton :to="testlink" color="primary" variant="solid">Button</UButton>
  </div>
</template>

<script setup>
const testlink = "https://gsremels.de";
</script>

<style lang="scss" scoped></style>
