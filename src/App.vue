<template>
  <v-app>
    <AppHeader />
    <v-main>
      <router-view />
    </v-main>
    <AppFooter />
  </v-app>
</template>

<script setup>
  // Import du magasin des armes
  import {useArmeStore} from "@/stores/armeStore";
  import AppHeader from "@/components/AppHeader.vue";
  import AppFooter from "@/components/AppFooter.vue";

  // Charge le magasin des armes
  const armeStore = useArmeStore();

  // Affiche le nom des armes dans la console
  for( let arme of armeStore.armes){
    console.log(arme.nom);
  }
</script>

