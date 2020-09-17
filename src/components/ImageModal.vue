<template>
    <div class="text-center">
        <div @click="dialog=true">
            <v-img max-height="200px" max-width="200px" :src="`${images[0].src}`"/>
        </div>
        <v-dialog
                v-model="dialog"
                width="500"
        >
            <v-card>
                <v-card-title class="headline grey lighten-2">
                    {{title}}
                </v-card-title>
                <v-card-text>
                    <v-carousel>
                        <v-carousel-item
                                v-for="(image,i) in images"
                                :key="i"
                                :src="image.src"
                                reverse-transition="fade-transition"
                                transition="fade-transition"
                        ></v-carousel-item>
                    </v-carousel>
                </v-card-text>
            </v-card>
        </v-dialog>
    </div>
</template>

<script>
  export default {
    name: "ImageModal",
    props: ["images", "title"],
    data () {
      return {
        dialog: false,
        items: [
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
          },
        ]
      }
    },
  }
</script>

<style scoped>

</style>