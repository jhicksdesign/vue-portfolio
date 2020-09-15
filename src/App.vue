<template>
  <v-app>
    <v-main>
      <HelloWorld/>
      <Nav/>
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';
import Nav from './components/Nav'

export default {
  name: 'App',

  components: {
    HelloWorld,
    Nav
  },

  data: () => ({
    //
  }),
};
</script>
