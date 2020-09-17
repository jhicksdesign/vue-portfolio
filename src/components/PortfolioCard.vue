<template>
    <v-container>
        <h1 :class="`text-center`">Portfolio</h1>
        <transition-group name="animated" enter-active-class="animated flipInY" leave-active-class="animated flipOutY">
            <v-row v-bind:key="card.id" align-content="center" v-for="card in projects" >
                <v-col cols="0" md="3"></v-col>
                <v-col cols="4" md="3">
                    <ImageModal ref="dialog" v-bind:images="card.images" v-bind:title="card.title"></ImageModal>
                </v-col>
                <v-col cols="8" md="6">
                    <h3>{{card.title}}</h3>
                    <p>{{card.content}}</p>
                </v-col>
            </v-row>
        </transition-group>
    </v-container>
</template>

<script>
  import 'animate.css'
  import ImageModal from './ImageModal'

  export default {
    name: "PortfolioCard",
    components: {ImageModal},
    props: ["projects"],
    data () {
      return {
        animated: true
      }
    },
  }
</script>

<style scoped>
</style>