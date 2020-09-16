<template>
  <v-app>
    <v-btn icon class="hidden-sm-and-up" @click="$refs.drawer.drawer = !$refs.drawer.drawer"><v-icon>mdi-menu</v-icon></v-btn>
    <Nav ref="drawer"/>
    <v-main>
      <PortfolioCard v-bind:projects="projects"/>
    </v-main>
  </v-app>
</template>

<script>
import Nav from './components/Nav'
import PortfolioCard from './components/PortfolioCard'

export default {
  name: 'App',

  components: {
    Nav,
    PortfolioCard,
  },
  data() {
    return {
      projects: [
        {
          id: 1,
          title: "Project One",
          content: "This is some content, isn't it rad, I needed ipsum, but that's just too bad.",
          image: "http://www.fillmurray.com/400/400"
        },
        {
          id: 2,
          title: "Project Two",
          content: "This is some content, isn't it rad, I needed ipsum, but that's just too bad.",
          image: "http://www.fillmurray.com/400/400"
        },
        {
          id: 3,
          title: "Project Three",
          content: "This is some content, isn't it rad, I needed ipsum, but that's just too bad.",
          image: "http://www.fillmurray.com/400/400"
        }
      ]
    }
  }
};
</script>
