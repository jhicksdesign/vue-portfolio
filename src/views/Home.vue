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
          id: 1,
          title: "Project One",
          content: "This is some content, isn't it rad, I needed ipsum, but that's just too bad.",
          image: "http://www.fillmurray.com/400/400",
          images: [
            {src: "http://www.fillmurray.com/350/450"},
            {src: "http://www.fillmurray.com/300/500"},
            {src: "http://www.fillmurray.com/250/550"}
          ]
        },
        {
          id: 2,
          title: "Project Two",
          content: "This is some content, isn't it rad, I needed ipsum, but that's just too bad.",
          image: "http://www.fillmurray.com/400/400",
          images: [
            {src: "http://www.fillmurray.com/450/450"},
            {src: "http://www.fillmurray.com/500/500"},
            {src: "http://www.fillmurray.com/550/550"}
          ]
        },
        {
          id: 3,
          title: "Project Three",
          content: "This is some content, isn't it rad, I needed ipsum, but that's just too bad.",
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
