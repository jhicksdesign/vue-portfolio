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
          title: "Deep Dive Coding \n June 2020 - Sept 2020",

          content: "Intensive ten week full stack bootcamp. Taught web development fundamentals, including HTML/CSS, React/Redux, Node, Express, and MySql. Emphasized importance and proper use of version control, as well as taught how agile programming methodologies work in hands on team environment.",
        },
          {title: "Associates of Applied Science - Multimedia and Web Design \n June 2017 - May 2019",
          content: "Learned basics of web design by creating multiple websites, using both WordPress as a CMS, and HTML/CSS/Javascript. Primarily focused on using bootstrap as main CSS framework, with some use of SASS as a css preprocessor. Course also taught skills in the Adobe Creative Suite using Illustrator, Photoshop, and After Effects."}
        ]
      }
    }
  }
</script>

<style scoped>

</style>