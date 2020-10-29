<template>
    <v-container>
        <v-row :key="i" align-content="center" v-for="(card, i) in projects">
            <v-col cols="0" md="3"></v-col>
            <v-col cols="4" md="3">
                <ImageModal ref="dialog" v-if="card.images"  v-bind:images="card.images" v-bind:title="card.title"></ImageModal>
            </v-col>
            <v-col cols="8" md="6">
                <h3>{{card.title}}</h3>
                <p>{{card.content}}</p>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
  import ImageModal from './ImageModal'

  export default {
    name: "PortfolioCard",
    components: {ImageModal},
    props: ["projects"],
    data () {
      return {
      }
    },
  }
</script>

<style scoped>
</style>