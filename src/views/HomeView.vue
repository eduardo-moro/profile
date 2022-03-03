<template>
  <div class="home">

    <v-container
        fluid
        class="white--text d-block mt-8 font--monospace main--title pb-0"
        :class="$vuetify.breakpoint.mobile ? 'px-6':'text-center'"
    >
      <div class="d-flex justify-center">

        <v-avatar size="max" class="pb-8 align-center">
          <v-img
              src="../assets/me.jpeg"
              max-width="280"
              class="profile-picture"
          >
          </v-img>
        </v-avatar>
      </div>

      <div class="d-block text-center">
        <h1>Welcome, I'm Eduardo Moro</h1>
        <h2>Fullstack developer</h2>
        <h3>Curitiba - PR - Brazil</h3>
        <h4>SDA student on UFPR</h4>

        <v-btn
            color="black"
            class="white--text mt-8 pb-0 mb-0"
            outlined
            target="_blank"
            href="/CV - EN - Eduardo Moro.docx"
        >
          Download my resume
          <v-icon/>
        </v-btn>
      </div>
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
