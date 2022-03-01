<template>
  <div class="home">

    <v-container
        fluid
        class="white--text d-block text-center mt-12 font--monospace main--title"
    >
      <h1>Welcome, I'm Eduardo Moro</h1>
    </v-container>

    <v-container
        fluid
        class="white--text d-block text-center mt-12 font--monospace main--title"
    >
      <v-btn>
        <p> Download CV </p>
        <v-icon />
      </v-btn>
    </v-container>

    <my-timeline/>

    <div
        class="py-16 black"
    >

    </div>
  </div>
</template>

<script>
// @ is an alias to /src

import MyTimeline from "@/components/MyTimeline";

export default {
  name: 'HomeView',
  components: {MyTimeline},
}
</script>

<style scoped>
.font--monospace {
  font-family: monospace;
}

.main--title {
  filter: drop-shadow(0 3px 5px black);

}

</style>
