<template>
  <v-app id="app">
    <main-header/>

    <v-main>
      <router-view/>
    </v-main>

    <main-footer />
  </v-app>
</template>

<script>

import MainHeader from "@/components/MainHeader";
import MainFooter from "@/components/MainFooter";
export default {
  name: 'App',
  components: {MainFooter, MainHeader},
  data: () => ({
    //
  }),
};
</script>

<style>
#app {
  background: #000000;
}
</style>
