<template>
  <div>
    <UContainer style="margin-top: 0.5rem">
      <AppHeader />
      <div class="prose dark:prose-invert">
        <h2 class="">{{ pageTitle }}</h2>
        <br />
      </div>
      <GenericLinks />
      <GroupLinks />
      <!-- <AdditionalLinks/> -->
      <!-- <AdditionalInfo/> -->
    </UContainer>
  </div>
</template>

<style lang="scss">
/*   */
</style>

<script setup>
import AppHeader from "./components/AppHeader/AppHeader.vue";
const pageTitle = "Boilerplate";

useHead({
  titleTemplate: (titleChunk) => {
    return titleChunk ? `${titleChunk} - GSR` : "GSR";
  },
  title: pageTitle,
  meta: [{ name: "description", content: "A simple description." }],
});
</script>
