<template>
  <v-app id="inspire">
    <v-navigation-drawer 
      v-model="drawer"
      :mobile-breakpoint="768"
      app
    >
      <v-list
        dense
        nav
        class="mt-15"
      >
        <v-list-item
          v-for="item in items"
          :key="item.title"
          :to="item.to"
          link
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar
      app
      elevation="0"
      color="#ffffff"
    >
      <v-container class="header-container pa-0">
          <v-row class="py-3">
          </v-row>
          <v-row class="px-3 text-h4">
          </v-row>
        </v-container>
    </v-app-bar>
    <v-main>
      <v-container
        fluid
        class="pa-0"
      >
        <router-view></router-view>
        <snackbar/>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
  export default {
    data: () => ({ 
      drawer: null,
      items: [
        { title: 'メニュー', icon: 'mdi-emoticon-outline', to: '/' },
        { title: 'メニュー', icon: 'mdi-emoticon-outline', to: '/about' },
      ]
    }),
    components: {
      'snackbar': require('@/components/Shared/Snackbar.vue').default,
    },
    mounted() {
      this.$store.dispatch('getTasks')
    }
  }
</script>

<style lang="sass">
  .header-container
    max-width: none !important
</style>