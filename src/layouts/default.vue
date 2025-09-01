<template>
  <AppHeader @toggle-drawer="drawer = !drawer" />
  <WorkDrawer v-model="drawer" />
  <v-main>
    <router-view />
  </v-main>
</template>
<script setup>
import { watch } from "vue";
import { useDisplay } from "vuetify";

const drawer = ref(true);

const { smAndDown } = useDisplay();
watch(smAndDown, (isSmAndDown) => (drawer.value = !isSmAndDown), {
  immediate: true,
});
</script>
