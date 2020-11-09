<template>
  <v-app>
    <v-btn style="z-index: 5" fixed icon class="hidden-sm-and-up mt-2" @click="$refs.drawer.drawer = !$refs.drawer.drawer"><v-icon>mdi-menu</v-icon></v-btn>
    <Nav ref="drawer"/>
    <v-main>
      <v-banner id="anchor" app style="background-color: rgba(139, 195, 74, .5)" class="text-center">Test</v-banner>
      <transition
              mode="out-in"
              enter-active-class="animate__animated animate__fadeInUpBig animate__fast"
              leave-active-class="animate__animated animate__lightSpeedOutLeft animate__fast"
              appear
      >
        <router-view/>
      </transition>
    </v-main>
  </v-app>
</template>

<script>
import Nav from './components/Nav'
import 'animate.css'

export default {
  name: 'App',

  components: {
    Nav,
  },
};
</script>

<style scoped>
</style>
