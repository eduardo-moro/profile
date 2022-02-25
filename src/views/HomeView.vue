<template>
  <div class="home">
    <v-img
        src="../assets/view.jpeg"
        max-height="100vh"
    >
      <v-container
          fluid
          class="white--text d-block text-md-center mt-12 font--monospace main--title"
      >
        <h1>Welcome, I'm Eduardo Moro</h1>
      </v-container>
    </v-img>

    <div
        class="py-16 black"
    >

    </div>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'HomeView',
  components: {}
}
</script>

<style scoped>
.setup-container {
  background: black;
  width: 100%;
}

.font--monospace {
  font-family: monospace;
}

.main--title {
  filter: drop-shadow(0 3px 5px black);

}

</style>
