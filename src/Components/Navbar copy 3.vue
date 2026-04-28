<template>

  <header class="flex justify-between bg-opacity-50 p-6 relative z-1
                  dark:bg-transparent
                 backdrop-blur-sm transition-colors duration-300" id="accueil">
  
    <!-- logo gauche -->
    <div class="text-2xl font-bold bg-linear-to-r from-blue-600 to-cyan-500 dark:from-blue-400 dark:to-cyan-400 bg-clip-text text-transparent">
      A. Jaffrelot Bizoux Abrivard
    </div>
  
    <!-- bouton hamburger mobile -->
    <div class="md:hidden z-30 flex items-center gap-3">
  
      <!-- Toggle dark mode visible sur mobile aussi -->
      <DarkModeToggle/>
  
      <button type="button"
        class="block hover:cursor-pointer focus:outline-none rounded-lg p-2
               bg-blue-100 hover:bg-blue-200
               dark:bg-blue-800/50 dark:hover:bg-blue-700/50
               transition-all duration-300"
        @click="toogleMenu">
  
        <div class="relative w-6 h-6">
          <span :class="['absolute left-0 w-6 h-0.5 transition-all duration-300 bg-blue-700 dark:bg-blue-200', isMenuOpen ? 'rotate-45 top-3' : 'top-1']"></span>
          <span :class="['absolute left-0 w-6 h-0.5 transition-all duration-300 bg-blue-700 dark:bg-blue-200', isMenuOpen ? 'opacity-0' : 'top-3 opacity-100']"></span>
          <span :class="['absolute left-0 w-6 h-0.5 transition-all duration-300 bg-blue-700 dark:bg-blue-200', isMenuOpen ? '-rotate-45 top-3' : 'top-5']"></span>
        </div>
      </button>
    </div>
  
    <!-- menu -->
    <nav :class="[
      'fixed inset-0 flex flex-col items-center justify-center',
      'md:relative md:bg-transparent md:flex md:flex-row md:items-center md:justify-between',
      'bg-white dark:bg-[#111827]',
      'transition-colors duration-300',
      isMenuOpen ? 'block' : 'hidden md:flex'
    ]">
      <ul class="flex flex-col items-center space-y-5 md:space-y-0 md:space-x-5 md:flex-row">
        <li v-for="menus in Menu" :key="menus.name">
          <a :href="menus.href"
             class="text-gray-700 hover:text-blue-600
                    dark:text-blue-100 dark:hover:text-blue-400
                    transition-all duration-300 text-xl font-medium md:text-base"
             @click="scrollToSection(menus.href)">
            {{ menus.name }}
          </a>
        </li>
      </ul>
  
      <!-- Toggle dark mode sur desktop -->
      <div class="hidden md:block ml-4">
        <DarkModeToggle/>
      </div>
    </nav>
  
  </header>
  
  </template>
  
  <script setup>
  import { ref } from 'vue';
  import DarkModeToggle from './DarkModeToggle.vue';
  
  const Menu = ref([
    { name: "Accueil", href: "#accueil" },
    { name: "Compétences", href: "#expérience" },
    { name: "Projets", href: "#projets" },
    { name: "Expériences", href: "#expérience" },
    { name: "Contact", href: "#contact" },
  ])
  
  const isMenuOpen = ref(false);
  const toogleMenu = () => {
    isMenuOpen.value = !isMenuOpen.value
  }
  
  const scrollToSection = (href) => {
    isMenuOpen.value = false;
    const section = document.querySelector(href);
    if (section) {
      section.scrollIntoView({ behavior: 'smooth' }); // ✅ corrigé aussi (srollInView → scrollIntoView)
    }
  }
  </script>