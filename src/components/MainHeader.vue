<template>
  <v-app-bar
      app
      color="#0000"
      dark
      elevation="0"
      class="gradient"
  >
    <v-spacer/>

    <div :key="link.href" v-for="link of links">
      <v-btn
          :href=link.href
          :target="link.isExternal ? '_blank':''"
          text
      >
        <span class="mr-2">{{ link.title }}</span>
      </v-btn>
    </div>

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
          isExternal: false
        },
        {
          href: "/about",
          title: "about",
          isExternal: false
        },
        {
          title: "linkedin",
          href: "https://www.linkedin.com/in/eduardomoro/?locale=en_US",
          isExternal: true
        },
        {
          href: "https://api.whatsapp.com/send?phone=5541991855670&text=Hey%20Eduardo%2C%20I%20came%20by%20your%20github",
          title: "whatsapp",
          isExternal: true
        },
        {
          href: "https://t.me/moroeduardo",
          title: "telegram",
          isExternal: true
        },
        {
          href: "mailto:eduardomoro1127@gmail.com",
          title: "gmail",
          isExternal: true
        },
        {
          href: "https://my.indeed.com/p/eduardohenriquep-hiffif5",
          title: "indeed",
          isExternal: true
        },
      ]
    }
  }
}
</script>

<style scoped>
.gradient {
    background: linear-gradient(180deg, rgba(0,0,0,1)0%, rgba(0,0,0,0) 75%, rgba(0,0,0,0) 100%);
}

</style>
