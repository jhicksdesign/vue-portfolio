<template>
    <v-container>
        <v-row :key="i" align-content="center" justify="center" v-for="(card, i) in projects">
            <v-col cols="12" md="4" class="justify-center" v-if="card.images">
                <ImageModal ref="dialog" v-if="card.images"  v-bind:images="card.images" v-bind:title="card.title"></ImageModal>
            </v-col>
            <v-col cols="12" md="6">
                <h3 style="white-space: pre-line">{{card.title}}</h3>
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