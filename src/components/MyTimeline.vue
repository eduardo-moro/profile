<template>
  <v-container class="">
    <v-timeline
        clipped
        v-for="event in timeline"
        :key="event.title"
    >
      <v-timeline-item small color="black">
        <template v-slot:opposite>
            <span class="headline font-weight-bold white--text">
              {{ event.year }}
            </span>
        </template>

        <v-card class="black">
          <v-card-title class="text-h5 white--text">
            {{ event.title }}
          </v-card-title>

          <v-card-text class="font-weight-bold white--text">
            {{ event.description }}
          </v-card-text>
        </v-card>
      </v-timeline-item>
    </v-timeline>
  </v-container>
</template>

<script>
export default {
  name: "my-timeline",
  data: () => {
    return {
      timeline: [
        {
          year: 2019,
        },
        {
          title: "UFPR - january",
          description: "System analysis and development"
        },
        {
          title: "Revenda Mais - july",
          description: "Backend internship"
        },
        {
          year: 2020,
        },
        {
          title: "Quadritech - march",
          description: "Fullstack junior developer"
        },
        {
          year: 2021
        },
        {
          title: "Ecritel - june",
          description: "Frontend mid developer"
        },
        {
          title: "Mavtek - october",
          description: "Fullstack mid developer"
        },
        {
          year: 2022
        }
      ]
    }
  }
}
</script>

<style scoped>

.theme--light.v-timeline::before {
  background: white;
  border-radius: 10px !important;
  opacity: 35%;
}

</style>
