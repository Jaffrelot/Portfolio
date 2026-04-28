<template>
  <div v-if="chargement">
    <chargement/>
  </div>

  <div v-else :class="isDark ? 'dark' : ''" class="min-h-screen">
    <div class="min-h-screen transition-colors duration-300
                bg-white text-gray-900
                dark:bg-gradient-to-br dark:from-gray-900 dark:via-blue-900 dark:to-gray-900 dark:text-white">

      <Navbar/>
      <Hero/>
      <Services/>
      <Experience/>
      <Projets/>
      <Contact/>
      <Footer/>
      <BasVersHaut/>
    </div>
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
import { useDarkMode } from '@/Components/useDarkMode'

import { onMounted, ref } from 'vue';
export default {
  name: 'App',
  components: {
    Navbar, Hero, Services,
    Experience, Projets, Contact, Footer, BasVersHaut, chargement
  },
  setup() {
    const chargement = ref(true);
    const { isDark } = useDarkMode();

    onMounted(() => {
      AOS.init({ duration: 800, once: false, offset: 100, easing: 'ease-in-out' });
      setTimeout(() => { chargement.value = false; }, 800);
    });

    return { chargement, isDark };
  }
}
</script>