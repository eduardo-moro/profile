<template>
  <div class="home">

    <v-container
        fluid
        class="white--text d-block mt-8 font--monospace main--title pb-0"
        :class="$vuetify.breakpoint.mobile ? 'px-6':'text-center'"
    >
      <h1>Welcome, I'm Eduardo Moro</h1>

      <v-btn
          color="black"
          class="white--text mt-4 pb-0 mb-0"
          outlined
          target="_blank"
          href="https://my.indeed.com/rdp/1cc218736026aab1/pdf"
      >
        Download  my resume
        <v-icon/>
      </v-btn>
    </v-container>

    <my-timeline/>
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
