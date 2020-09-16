<template>
    <v-container>
        <h1 :class="`text-center`">Portfolio</h1>
        <v-row v-bind:key="card.id" align-content="center" v-for="card in projects">
            <v-col cols="0" md="3"></v-col>
            <v-col cols="4" md="3">
                <v-img max-height="200px" max-width="200px" :src="`${card.image}`"/>
            </v-col>
            <v-col cols="8" md="6">
                <h3>{{card.title}}</h3>
                <p>{{card.content}}</p>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
  export default {
    name: "PortfolioCard",
    props: ["projects"]
  }
</script>

<style scoped>
</style>