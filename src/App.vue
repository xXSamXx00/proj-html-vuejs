<template>
  <div id="app">
    <SiteHeader :menu="menuHeader"/>
    <SiteMain :courses="cardCourses" :brands="brands" :blogs="blogs"/>
    <SiteFooter/>
  </div>
</template>

<script>
import SiteHeader from './components/SiteHeader.vue'
import SiteMain from './components/SiteMain.vue'
import SiteFooter from './components/SiteFooter.vue'

export default {
  name: 'App',
  components: {
    SiteHeader,
    SiteMain,
    SiteFooter
  },
  data() {
    return {
      menuHeader: ["Home", "Pages", "Courses", "Features", "Blog", "Shop"],
      cardCourses: [
        {
          image: "1",
          price: "$40",
          title: "Learning to Write as a Professional Author",
          lessons: "20",
          students: "50"
        },
        {
          image: "2",
          price: "Free",
          title: "Customer-centric Info-Tech Strategies",
          lessons: "24",
          students: "769"
        },
        {
          image: "3",
          price: "$19",
          title: "Open Programming Courses for Everyone: Python",
          lessons: "17",
          students: "62"
        },
        {
          image: "4",
          price: "$26",
          title: "Academic Listening and Note-taking",
          lessons: "6",
          students: "67"
        },
        {
          image: "5",
          price: "$39",
          title: "Master jQuery in a Short Period of Time",
          lessons: "6",
          students: "51",
        },
        {
          image: "6",
          price: "$59",
          title:  "Introduction to Javascript for Beginners",
          lessons: "14",
          students: "76"
        }
      ],
      brands: ["1", "2", "3", "4", "5", "6"],
      blogs: [
        {
          image: "1",
          title: "Brush Strokes Energize Trees in Paintings",
          views: "688"
        },
        {
          image: "2",
          title: "Pocket-Sized Notebooks Hold Miniature Paintings",
          views: "603"
        },
        {
          image: "3",
          title: "Connection Between Self-Portraits and Identity",
          views: "397"
        },
      ]
    }
  }
}
</script>

<style lang="scss">
@import "../node_modules/bootstrap/scss/bootstrap.scss";
html {
  scroll-behavior: smooth;
}
body {
  font-family: Arial, Helvetica, sans-serif;
}
</style>