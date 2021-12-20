<template>
  <v-app>
    <Header></Header>

    <v-main>
      <!---HeroSection -->
      <HeroComponent />
            <!---About Us -->
      <About />
      <Portfolio />
      <Project />
      <Galery />
      <Contact />
      <Footer />
    </v-main>
  </v-app>
</template>

<script>

import Header from "./components/Header.vue"
import HeroComponent from "./components/Hero.vue"
import About from "./components/AboutUs.vue"
import Portfolio from "./components/Porfolio.vue"
import Project from "./components/Project.vue"
import Galery from "./components/Galery.vue"
import Contact from "./components/Contact.vue"
import Footer from "./components/Footer.vue"
export default {
  name: 'App',
  components:{Header,HeroComponent,About,Portfolio,Project,Galery,Contact,Footer},

};
</script>
