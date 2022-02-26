<template>
  <div class="home">

    <v-container
        fluid
        class="white--text d-block text-md-center mt-12 font--monospace main--title"
    >
      <h1>Welcome, I'm Eduardo Moro</h1>
    </v-container>

    <v-container class="mt-16">
      <v-timeline
          clipped
      >
        <v-timeline-item small color="black">
          <template v-slot:opposite>
            <span class="headline font-weight-bold white--text">
              2019
            </span>
          </template>

          <v-card class="black">
            <v-card-title class="text-h5 white--text">
              UFPR
            </v-card-title>

            <v-card-text class="font-weight-bold white--text">
              Minnor degree in system analisis and development
            </v-card-text>
          </v-card>
        </v-timeline-item>

        <v-timeline-item small color="black">
          <template v-slot:opposite>
            <span class="headline font-weight-bold white--text">
              2019
            </span>
          </template>

          <v-card class="black ">
            <v-card-title class="text-h5 white--text justify-end">
              UFPR
            </v-card-title>

            <v-card-text class="font-weight-bold white--text text-end">
              Minnor degree in system analisis and development
            </v-card-text>
          </v-card>
        </v-timeline-item>
      </v-timeline>
    </v-container>

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
.font--monospace {
  font-family: monospace;
}

.main--title {
  filter: drop-shadow(0 3px 5px black);

}

.theme--light.v-timeline::before {
  background: white;
  border-radius: 10px !important;
  opacity: 35%;
}

</style>
