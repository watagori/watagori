<template>
  <div>
    <v-navigation-drawer v-model="drawer" app width="300">
      <v-navigation-drawer
        v-model="drawer"
        absolute
        color="grey lighten-3"
        mini-variant
      >
        <nuxt-link to="/makeroom">
          <v-avatar
            class="d-block text-center mx-auto mt-4"
            color="grey darken-1"
            size="36"
          >
            <v-icon dark to> mdi-plus-circle </v-icon>
          </v-avatar>
        </nuxt-link>

        <v-divider class="mx-3 my-5"></v-divider>
        <template v-for="num in 5">
          <v-avatar
            class="d-block text-center mx-auto mb-9"
            color="grey lighten-1"
            size="28"
            :key="num"
          >
            <span>{{ num }}</span></v-avatar
          >
        </template>
      </v-navigation-drawer>
      <v-sheet color="grey lighten-5" height="128" width="100%"></v-sheet>

      <v-list class="pl-14" shaped>
        <v-list-item v-for="n in 8" :key="n" link>
          <v-list-item-content>
            <v-list-item-title>Item {{ n }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-navigation-drawer app clipped right>
      <v-list>
        <v-list-item v-for="n in 5" :key="n" link>
          <v-list-item-content>
            <v-list-item-title>Item {{ n }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>

<script>
export default {
  data: () => ({ drawer: null }),
}
</script>

<style lang="scss" scoped></style>
