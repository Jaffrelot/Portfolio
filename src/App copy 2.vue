<template>

  <!-- chargement -->

  <div v-if="chargement">
    <chargement/>
  </div>

  <div v-else class="min-h-screen bg-linear-to-br from-gray-900 via-blue-900 to-gray-900">

    
    <Navbar/>
    <Projets/>
    

  </div>



</template>

<script>
import AOS from 'aos';
import 'aos/dist/aos.css';
import Navbar from './Components/Navbar.vue'
import Projets from './Components/Projets.vue'
import chargement from './Components/chargement.vue'
import { onMounted,ref } from 'vue';
export default {
  name:'App',
  components:{
    Navbar,
    Projets,
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