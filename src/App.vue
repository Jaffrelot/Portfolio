<template>

<div v-if="chargement">
  <chargement/>
</div>

<div v-else class="min-h-screen bg-linear-to-br from-gray-900 via-blue-900 to-gray-900">
    <Navbar/>
    <Hero/>
    <Services/>
    <Experience/>
    <Projets/>
    <Contact/>
    <Footer/>
    <BasVersHaut/>
</div>


</template>

<script>
import AOS from 'aos';
import 'aos/dist/aos.css';
import Navbar from './Components/Navbar.vue'
import Hero from './Components/Hero.vue'
import Services from './Components/Services.vue'
import Experience from './Components/Experience.vue'
import Projets from './Components/Projets.vue'
import Contact from './Components/Contact.vue'
import Footer from './Components/Footer.vue'
import BasVersHaut from './Components/BasVersHaut.vue'
import chargement from './Components/chargement.vue'

import { onMounted,ref } from 'vue';
export default {
  name:'App',
  components:{
    Navbar,
    Hero,
    Services,
    Experience,
    Projets,
    Contact,
    Footer,
    BasVersHaut,
    chargement
  },
  setup(){
    const chargement = ref(true);

    onMounted(()=>{
      AOS.init({
      duration:800,
      once: false,
      offset:100,
      easing: 'ease-in-out'
    });

    setTimeout(() => {
      chargement.value = false;
    }, 800);


    })
    return {chargement};

    
  }
}
</script>

<style>

</style>