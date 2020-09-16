<template>
  <v-app>
    <v-btn icon class="hidden-sm-and-up" @click="$refs.drawer.drawer = !$refs.drawer.drawer"><v-icon>mdi-menu</v-icon></v-btn>
    <Nav ref="drawer"/>
    <v-main>
      <router-view></router-view>
    </v-main>
  </v-app>
</template>

<script>
import Nav from './components/Nav'

export default {
  name: 'App',

  components: {
    Nav,
  },
};
</script>
