<template>
    <div class="text-center">
        <v-sheet class="ma-auto test" max-height="200px" max-width="200px" elevation="5" @click="dialog=true">
            <v-hover
                    value>
                <v-img class="ma-auto" cover max-height="200px" max-width="200px" :src="`${images[0].src}`">
                </v-img>
            </v-hover>
        </v-sheet>
        <v-dialog
                v-model="dialog"
                width="600"
        >
            <v-card>
                <v-card-title class="headline grey lighten-2 justify-center">
                    {{title}}
                </v-card-title>
                <v-card-text
                        class="px-0">
                    <v-carousel>
                        <v-carousel-item
                                v-for="(image,i) in images"
                                :key="i"
                                :src="image.src"
                                reverse-transition="fade-transition"
                                transition="fade-transition"
                                contain
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
      }
    },
  }
</script>

<style scoped>
    .test {
        cursor: pointer;
    }
</style>