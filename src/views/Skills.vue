<template>
    <v-container class="flex">
        <v-row align="center" justify="center" class="fill-height">
            <v-layout class="d-flex text-center mx-auto">
                <SkillCard v-bind:skills="skills"></SkillCard>
            </v-layout>
        </v-row>
    </v-container>
</template>

<script>
  import SkillCard from '../components/SkillCard'

  export default {
    name: "Skills",
    components: {SkillCard},
    data () {
      return {
        skills: [
          {
            icon: "mdi-react",
            title: "React"
          },
          {
            icon: "mdi-react",
            title: "Redux"
          },
          {
            icon: "mdi-vuejs",
            title: "Vue.js"
          },
          {
            icon: "mdi-vuetify",
            title: "Vuetify"
          },
          {
            icon: "mdi-language-javascript",
            title: "JavaScript"
          },
          {
            icon: "mdi-language-typescript",
            title: "TypeScript"
          },
          {
            icon: "mdi-language-python",
            title: "Python"
          },
          {
            icon: "mdi-bootstrap",
            title: "Bootstrap"
          },
          {
            icon: "mdi-wordpress",
            title: "WordPress"
          },
          {
            icon: "mdi-nodejs",
            title: "Node.js"
          },
          {
            icon: "mdi-database",
            title: "MySQL"
          },
          {
            icon: "mdi-server",
            title: "Express"
          },
          {
            icon: "mdi-git",
            title: "GIT"
          },
          {
            icon: "mdi-docker",
            title: "Docker"
          }

        ]
      }
    }
  }
</script>

<style scoped>
    .flex {
        height: 100%;
    }
</style>
