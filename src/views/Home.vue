<template>
  <div class="home my-auto">
    <PortfolioCard v-bind:projects="projects"/>
  </div>
</template>

<script>
import PortfolioCard from '../components/PortfolioCard'

export default {
  name: 'Home',
  components: {
    PortfolioCard
  },
  data() {
    return {
      projects: [
        {
          title: "ConcertCrawl",
          content: "Website designed as capstone project for Deep Dive Coding full stack bootcamp, was a culmination of all the technologies learned during the bootcamp. Developed in a group of three, coordinated using GIT as a version control software and Asana to facilitate development in an agile fashion. Front end was designed using React and Redux. Backend was designed using node, express, and MySQL for the database. ",
          image: "../assets/2ts88b2.png",
          images: [
            {src: "http://www.fillmurray.com/350/450"},
            {src: "http://www.fillmurray.com/300/500"},
            {src: "http://www.fillmurray.com/250/550"}
          ]
        },
        {
          title: "Suzy S. Photography",
          content: "Portfolio project that I created as a solo project to help a beginner photographer get more exposure. Designed using HTML/CSS and some Javascript, used bootstrap for a css framework and express was used to set up the mail form functionality.",
          image: "http://www.fillmurray.com/400/400",
          images: [
            {src: "http://www.fillmurray.com/450/450"},
            {src: "http://www.fillmurray.com/500/500"},
            {src: "http://www.fillmurray.com/550/550"}
          ]
        },
        {
          title: "Missouri Kids",
          content: "Capstone website for my web design associates, designed using WordPress with a team of eight other students. Website was a complete redesign for the non profit organization Missouri Kids, my main role on this project was designing the hom page and overall look and feel of the website.",
          image: "http://www.fillmurray.com/400/400",
          images: [
            {src: "http://www.fillmurray.com/450/450"},
            {src: "http://www.fillmurray.com/500/500"},
            {src: "http://www.fillmurray.com/550/550"}
          ]
        }, {
          title: "JHicks Design",
          content: "First portfolio project I designed for myself, design using HTML/CSS with some Javascript, used bootstrap for css framework. Was a project to tie together my creative skills with my web design skills to sell myself as a developer.",
          image: "http://www.fillmurray.com/400/400",
          images: [
            {src: "http://www.fillmurray.com/450/450"},
            {src: "http://www.fillmurray.com/500/500"},
            {src: "http://www.fillmurray.com/550/550"}
          ]
        }

      ]
    }
  }
}
</script>
