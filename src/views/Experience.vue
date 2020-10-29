<template>
    <div class="experience my-auto">
        <PortfolioCard v-bind:projects="experience"/>
    </div>
</template>

<script>
  import PortfolioCard from '../components/PortfolioCard'

  export default {
    name: "Experience",
    components: {PortfolioCard},
    data() {
      return {
        experience: [{
          title: "Test",
          content: "Test description",
        },
          {title: "Test two",
          content: "test two description"}
        ]
      }
    }
  }
</script>

<style scoped>

</style>