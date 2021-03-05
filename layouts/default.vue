<template>
  <v-app id="inspire">
    <the-system-bar></the-system-bar>
    <the-app-bar></the-app-bar>
    <the-navigation-bar></the-navigation-bar>
    <v-main>
      <nuxt />
    </v-main>
  </v-app>
</template>

<script>
import TheAppBar from '~/components/TheAppBar.vue'
import TheNavigationBar from '~/components/TheNavigationBar.vue'
import TheSystemBar from '~/components/TheSystemBar.vue'
export default {
  components: { TheSystemBar, TheAppBar, TheNavigationBar },
  data: () => ({ drawer: null }),
}
</script>
