<template>
  <v-app id="app">
    <main-header/>

    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>

import MainHeader from "@/components/MainHeader";
export default {
  name: 'App',
  components: {MainHeader},
  data: () => ({
    //
  }),
};
</script>

<style>
#app {
  background: #101010;
}
</style>
