<template>
  <v-app>
    <v-btn icon class="hidden-sm-and-up" @click="$refs.drawer.drawer = !$refs.drawer.drawer"><v-icon>mdi-menu</v-icon></v-btn>
    <Nav ref="drawer"/>
    <v-main>
      <transition
              mode="out-in"
              enter-active-class="animate__animated animate__fadeInUpBig"
              leave-active-class="animate__animated animate__lightSpeedOutLeft"
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
