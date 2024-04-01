<template>
  <div class="prose dark:prose-invert">
    <h2 class="text-primary">Über diese Seite</h2>
    <div>
      Diese Seite wurde vom Technikteam erstellt und läuft auf dem IServ.
    </div>

    <h3 class="">Weitere Infos</h3>
    <ul>      
      <li>
        Die Seite enthält Links zum normalen IServ-Modul.
      </li>
      <li>Wenn man auf den Link klickt, wird der Gruppen- und Datumsfilter im IServ-Modul entsprechend voreingestellt.</li>
      <li>Diese Seite verarbeitet selbst keine Daten, sondern stellt nur Links mit Hilfe der Gruppen-ID und des Datums bereit.</li>

    </ul>
    <UAccordion
    color="primary"
    variant="ghost"
    size="2xs"
    :items="[{ label: 'Admin-Info', content: 'Bei Gruppenwechseln (Schuljahreswechsel) müssen die neuen IDs im Ordner einetragen werden. Neu kompilieren?' }, { label: 'Quellcode', content: 'github ...' },]"
  />
  </div>
</template>

<script setup></script>

<style lang="scss" scoped></style>
