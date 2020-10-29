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
          image: "/static/concert-crawl/FooSearch.png",
          images: [
            {src: "/static/concert-crawl/FooSearch.png"},
            {src: "/static/concert-crawl/SearchExample.png"},
            {src: "/static/concert-crawl/SaveConcerts.png"}
          ]
        },
        {
          title: "Suzy S. Photography",
          content: "Portfolio project that I created as a solo project to help a beginner photographer get more exposure. Designed using HTML/CSS and some Javascript, used bootstrap for a css framework and express was used to set up the mail form functionality.",
          image: "/static/suzy-s-photography/MainImage.jpeg",
          images: [
            {src: "/static/suzy-s-photography/MainImage.jpeg"},
            {src: "/static/suzy-s-photography/PortfolioGrid.jpg"},
            {src: "/static/suzy-s-photography/Contact.png"}
          ]
        },
        {
          title: "Missouri Kids",
          content: "Capstone website for my web design associates, designed using WordPress with a team of eight other students. Website was a complete redesign for the non profit organization Missouri Kids, my main role on this project was designing the hom page and overall look and feel of the website.",
          image: "/static/missouri-kids/MainImage.png",
          images: [
            {src: "/static/missouri-kids/MainImage.png"},
            {src: "/static/missouri-kids/MissouriStatement.png"},
            {src: "/static/missouri-kids/Sponsors.png"}
          ]
        }, {
          title: "JHicks Design",
          content: "First portfolio project I designed for myself, design using HTML/CSS with some Javascript, used bootstrap for css framework. Was a project to tie together my creative skills with my web design skills to sell myself as a developer.",
          image: "/static/jhicks-design/Banner.jpg",
          images: [
            {src: "/static/jhicks-design/Banner.jpg"},
            {src: "/static/jhicks-design/JsPython.png"},
            {src: "/static/jhicks-design/Design.png"}
          ]
        }

      ]
    }
  }
}
</script>
