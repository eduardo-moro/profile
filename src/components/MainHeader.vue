<template>
  <v-app-bar
      app
      color="#0000"
      dark
      elevation="0"
      class="gradient"
  >
    <v-spacer/>

    <template v-if="$vuetify.breakpoint.mobile">

      <div :key="link.href" v-for="link of links">
        <v-btn
            small
            :href=link.href
            :target="link.isExternal ? '_blank':''"
            text
        >
          <v-icon :title="link.title" class="mr-2">{{ link.icon }}</v-icon>
        </v-btn>
      </div>
    </template>

    <template v-else>
      <div :key="link.href" v-for="link of links">
        <v-btn
            :href=link.href
            :target="link.isExternal ? '_blank':''"
            text
        >
          <span class="mr-2">{{ link.title }}</span>
        </v-btn>
      </div>
    </template>

    <v-spacer/>
  </v-app-bar>
</template>

<script>
export default {
  name: "main-header",
  data() {
    return {
      links: [
        {
          href: "/",
          title: "home",
          icon: "fa-home",
          isExternal: false
        },
        {
          href: "https://github.com/eduardo-moro",
          title: "github",
          icon: "fa-github",
          isExternal: true
        },
        {
          href: "https://www.linkedin.com/in/eduardomoro/?locale=en_US",
          title: "linkedin",
          icon: "fa-linkedin",
          isExternal: true
        },
        {
          href: "https://api.whatsapp.com/send?phone=5541991855670&text=Hey%20Eduardo%2C%20I%20came%20by%20your%20github",
          title: "whatsapp",
          icon: "fa-whatsapp",
          isExternal: true
        },
        {
          href: "https://t.me/moroeduardo",
          title: "telegram",
          icon: "fa-telegram",
          isExternal: true
        },
        {
          href: "mailto:eduardomoro1127@gmail.com",
          title: "gmail",
          icon: "fa-envelope",
          isExternal: true
        },
        {
          href: "https://my.indeed.com/p/eduardohenriquep-hiffif5",
          title: "indeed",
          icon: "fa-info",
          isExternal: true
        },
      ]
    }
  }
}
</script>

<style scoped>
.gradient {
  background: black;
}

</style>
