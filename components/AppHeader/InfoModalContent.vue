<template>
  <div class="prose dark:prose-invert">
    <h2 class="text-primary">Über diese Seite</h2>
    <div>Diese Seite wurde von ...... erstellt und läuft wo?.....</div>

    <h3 class="">Weitere Infos</h3>
    <ul>
      <li>Infos zur Seite...</li>
      <li>Info 1</li>
      <li>Info 2</li>
    </ul>

    <UAccordion color="primary" variant="ghost" size="2xs" :items="items">
      <template #item="{ item }">
        {{ item.description }}
      </template>

      <template #admininfo>
        <div>Info for Admins...</div>
      </template>

      <template #sourcecode>
        <div>
          This project is licenced under the MIT License
          <ULink to="https://choosealicense.com/licenses/mit/" target="_blank"
            >(details) </ULink
          >.
          <br />
          Source code available at
          <ULink to="https://github.com/EasilySidetracted/" target="_blank"
            >github.com/EasilySidetracted</ULink
          >.
        </div>
      </template>
    </UAccordion>
  </div>
</template>

<script setup>
const items = [
  {
    label: "Admin-Info",
    icon: "i-heroicons-information-circle",
    slot: "admininfo",
  },
  {
    label: "Quellcode",
    icon: "i-heroicons-command-line",
    slot: "sourcecode",
  },
];
</script>

<style lang="scss" scoped></style>
