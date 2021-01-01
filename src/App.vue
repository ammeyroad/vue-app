<template>
  <div id="app">
    <router-view/><br class="mt-4">
    <hero />

     <Footer />
  </div>
</template>

<script>
import Footer from "@/components/Footer.vue"
import Hero from './components/Hero.vue'


export default {
  components: {
    Footer,


   
  }
}

   Hero
 </script>
   