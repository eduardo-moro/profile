<template>
  <v-app id="app">
    <mobile-header v-if="$vuetify.breakpoint.mobile"/>
    <main-header v-else/>

    <v-main>
      <router-view/>
    </v-main>

    <main-footer />
  </v-app>
</template>

<script>

import MainHeader from "@/components/MainHeader";
import MobileHeader from "@/components/MobileHeader";
import MainFooter from "@/components/MainFooter";
export default {
  name: 'App',
  components: {MainFooter, MobileHeader, MainHeader},
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
