<template>
    <v-app-bar color="green" class="">
      <v-app-bar-nav-icon variant="text" @click.stop="rail = !rail"></v-app-bar-nav-icon>

      <v-toolbar-title>БЮДЖЕТ</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon="mdi-dots-vertical" variant="text"></v-btn>
    </v-app-bar>

    <v-navigation-drawer absolute permanent :rail="rail" v-model="drawer">
      <v-divider></v-divider>
      <v-list-item prepend-icon="mdi-cash" link to="/" title="Главная"></v-list-item>
      <v-list-item prepend-icon="mdi-trending-up" link to="/income" title="Доход"></v-list-item>
      <v-list-item prepend-icon="mdi-trending-down" link to="/expense" title="Расход"></v-list-item>
    </v-navigation-drawer>
</template>

<script lang="js" setup>
import { ref } from 'vue';

const drawer = ref(true);
const rail = ref(false);

</script>