<template>
  <div class="prose dark:prose-invert">
    <h2 class="text-primary">Über diese Seite</h2>
    <div>
      Diese Seite wurde vom Technikteam erstellt und läuft auf dem IServ.
    </div>

    <h3 class="">Weitere Infos</h3>
    <ul>
      <li>Die Seite enthält Links zum normalen IServ-Modul.</li>
      <li>
        Wenn man auf den Link klickt, wird der Gruppen- und Datumsfilter im
        IServ-Modul entsprechend voreingestellt.
      </li>
      <li>
        Diese Seite verarbeitet selbst keine Daten, sondern stellt nur Links mit
        Hilfe der Gruppen-ID und des Datums bereit.
      </li>
    </ul>

    <UAccordion color="primary" variant="ghost" size="2xs" :items="items">
      <template #item="{ item }">
        <p class="italic text-gray-900 dark:text-white text-center">
          {{ item.description }}
        </p>
      </template>

      <template #sourcecode>
        <div >       

          <p >
            <a href="https://github.com/EasilySidetracted/nuxt3-boilerplate"
              >github.com/EasilySidetracted</a
            >
          </p>
        </div>
      </template>

      <template #admininfo>
        <div class="text-gray-900 dark:text-white text-center">
          <Logo class="w-auto h-8 mx-auto" />

          <p class="text-sm text-gray-500 dark:text-gray-400 mt-2">
            <a href="Fully styled and customizable components for Nuxt."
              >Link!</a
            >
          </p>
        </div>
      </template>
    </UAccordion>

    <UAccordion
      color="primary"
      variant="ghost"
      size="2xs"
      :items="[
        {
          label: 'Admin-Info',
          content: 'Hinweise für Admins...',
        },
        { label: 'Quellcode', content: link },
      ]"
    />
  </div>
</template>

<script setup>
const items = [
  {
    label: "Quellcode",
    icon: "i-heroicons-command-line",    
    slot: "sourcecode",
  },
  {
    label: "Admin-Info",
    icon: "i-heroicons-information-circle",    
    slot: "admininfo",
  },
];
</script>

<style lang="scss" scoped></style>
