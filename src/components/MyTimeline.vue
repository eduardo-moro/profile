<template>
  <v-container class="mt-0 pt-0">
    <v-timeline
        clipped
        :dense="$vuetify.breakpoint.mobile"
        v-for="event in timeline"
        :key="event.title"
    >
      <v-timeline-item small color="black">
        <template v-slot:opposite>
            <span class="headline font-weight-bold white--text">
              {{ event.year }}
            </span>
          <span class="subtitle-1  font-weight-thin white--text">
              {{ event.month }}
            </span>
        </template>

        <v-card class="black">
          <v-card-title class="title pb-4 white--text">
            {{ event.title }}
          </v-card-title>

          <v-card-subtitle class="subtitle-2 pb-1 white--text">
            <p v-html=" event.subtitle "/>
          </v-card-subtitle>

          <v-card-text class="white--text">
            <p v-html=" event.description "/>
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
          month: "january",
          title: "UFPR",
          subtitle: "Minor degree - System analysis and development",
          description:
              "<li>Here I learned the fundaments of programming logic, computer architecture, web topology and lots of soft skills </li>" +
              "<li>Also I learned Pascal, C, assembly, PHP, HTML, CSS, and a bit of react and react native. </li>"
        },
        {
          month: "july",
          title: "Revenda Mais",
          subtitle: "Backend internship",
          description:
              "<li>Worked on an admnistrative tool based on YII 1.0, used by 300+ car stores over the country</li>" +
              "<li>Made a database migration from postgresSQL to SQLite</li>" +
              "<li>Worked mainly on spreadsheet pages for costumers and internal use</li>" +
              "<li>Started an angular.js project to test the use of the framework on some desired scenarios</li>"
        },
        {
          year: 2020,
        },
        {
          month: "june",
          title: "Quadritech",
          subtitle: "Fullstack junior developer",
          description:
              "<li>Worked mainly on an administrative tool based on YII 1.1 used by 140+ driving schools and \"DETRAN\";</li>" +
              "<li>Worked on a vue 2.0 and lumen based application used by more than 600 students daily</li>" +
              "<li>Restored a 2011 project based on php 5.6 and YII 1.0 and migrated to php 7.4, updated all the design of the page (I don't have info about the current status of the project)</li>" +
              "<li>Created a face recognition and life validation API using python and openCV</li>" +
              "<li>Created react native based applications as proposal to replace an older native projects</li>" +
              "<li>Created AWS Console Scripts mainly involving media storage and search optimization</li>" +
              "<li>Helped and oriented newer developers</li>" +
              "<li>Active participation on company meetings, mainly on project decisions</li>" +
              "<li>Code review of newer developers</li>"
        },
        {
          year: 2021
        },
        {
          month: "april",
          title: "Confidential",
          subtitle: "Freelance fullstack developer",
          description:
              "<li>I created a Golang backend with Gin and ElasticSearch used by over 10k users</li>" +
              "<li>My platform consults 6 diferent public APIs to validate brazilian medical documents</li>" +
              "<li>Created react native template pages using navigator 4 and axios</li>" +
              "<li>Created react template pages</li>"
        },
        {
          month: "july",
          title: "Ecritel",
          subtitle: "Frontend mid developer",
          description:
              "<li>Developed vue template pages using nuxt and vue 3</li>" +
              "<li>Created HTML Template creation used on magento application</li>" +
              "<li>Created templates using figma documented style guides</li>" +
              "<li>Created components used on internal frontend framework using tailwind</li>" +
              "<li>Full remote job</li>"
        },
        {
          month: "october",
          title: "Mavtek",
          subtitle: "Fullstack mid developer",
          description:
              "<li>I solved multiple tasks related to live streaming pages used by over +3m active members and +89k models</li>" +
              "<li>Improved multiple soft skills such as communication</li>" +
              "<li>Full remote job, with all the comunication done in english</li>" +
              "<li>Refactored complex legacy code for US tax forms</li>" +
              "<li>Monitored system performance and logs</li>"
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

li {
  padding-bottom: 0;
}

</style>
