<template>

<header class="flex justify-between bg-opacity-50 p-6 relative z-1" id="accueil">

<!-- logo gauche -->
 <div class="text-2xl font-bold bg-linear-to-r from-blue-400 to-cyan-400 bg-clip-text text-transparent">
    A. Jaffrelot Bizoux Abrivard
 </div>

 <!-- menu droite bouton -->
  <div class="md:hidden z-30">
    <button type="button" class="block hover:cursor-pointer focus:outline-none rounded-lg p-2 bg-blue-800/50 hover:bg-blue-700/50 transition-all duration-300" @click="toogleMenu">

      <!-- ligne comme superposé comme bouton -->
      <div class="relative w-6 h-6">

        <!-- ligne 1 -->
        <span :class="['absolute left-0 w-6 h-0.5 bg-blue-200 transition-all duration-300',isMenuOpen? 'rotate-45 top-3' : 'top-1']"></span>
        
        <!-- ligne 2 -->
        <span :class="['absolute left-0 w-6 h-0.5 bg-blue-200 transition-all duration-300',isMenuOpen? 'opacity-0' : 'top-3 opacity-100']"></span>
        
        <!-- ligne 3 -->
        <span :class="['absolute left-0 w-6 h-0.5 bg-blue-200 transition-all duration-300',isMenuOpen? '-rotate-45 top-3' : 'top-5']"></span>
        

      </div>

    </button>
  </div>

  <!-- menu -->
   <nav :class="['fixed inset-0 bg-[#111827] flex flex-col items-center justify-center md:relative md:bg-transparent md:flex d:justify-between md:flex-row',isMenuOpen? 'block' : 'hidden']">
    <ul class="flex flex-col items-center space-y-5 md:space-y-0 md:space-x-5 md:flex-row">
      <li v-for="menus in Menu" :key="menus.name">
        <a :href="menus.href" class="text-blue-100 hover:text-blue-400 transition-all duration-300 text-xl font-medium md:text-base" @click="scrollToSection(menus.href)">{{ menus.name }}</a>
      </li>
    </ul>
   </nav>



</header>




</template>

<script setup>
import {ref} from 'vue';

const Menu = ref([
  {name:"Accueil",href:"#accueil"},
  {name:"Compétences",href:"#expérience"},
  {name:"Projets",href:"#projets"},
  {name:"Expériences",href:"#expérience"},
  {name:"Contact",href:"#contact"},
])

const isMenuOpen = ref(false);
const toogleMenu = ()=>{
  isMenuOpen.value = ! isMenuOpen.value
}

const scrollToSection = (href)=>{
  isMenuOpen.value = false;
  const section = document.querySelector(href);
  if(section){
    section.srollInView({behavior: 'smooth'});
  }
}

// this.isMenuOpen = !this.isMenuOpen

</script>