<template>
    <nav class="bg-gray-900 text-white">
      <div class="max-w-7xl mx-auto px-4">
  
        <div class="flex justify-between items-center h-16">
  
          <!-- Logo -->
          <div class="text-xl font-bold">
            MonApp
          </div>
  
          <!-- Bouton Hamburger -->
          <button
            @click="toggleMenu"
            class="md:hidden flex flex-col justify-center items-center w-8 h-8 focus:outline-none"
          >
            <span
              :class="[
                'block w-6 h-0.5 bg-white transition-all duration-300',
                isOpen ? 'rotate-45 translate-y-1.5' : ''
              ]"
            ></span>
  
            <span
              :class="[
                'block w-6 h-0.5 bg-white my-1 transition-all duration-300',
                isOpen ? 'opacity-0' : ''
              ]"
            ></span>
  
            <span
              :class="[
                'block w-6 h-0.5 bg-white transition-all duration-300',
                isOpen ? '-rotate-45 -translate-y-1.5' : ''
              ]"
            ></span>
          </button>
  
          <!-- Menu Desktop -->
          <div class="hidden md:flex space-x-6">
            <a href="#" class="hover:text-blue-400">Accueil</a>
            <a href="#" class="hover:text-blue-400">Services</a>
            <a href="#" class="hover:text-blue-400">À propos</a>
            <a href="#" class="hover:text-blue-400">Contact</a>
          </div>
  
        </div>
  
        <!-- Menu Mobile -->
        <transition
          enter-active-class="transition-all duration-300 ease-out"
          enter-from-class="max-h-0 opacity-0"
          enter-to-class="max-h-60 opacity-100"
          leave-active-class="transition-all duration-300 ease-in"
          leave-from-class="max-h-60 opacity-100"
          leave-to-class="max-h-0 opacity-0"
        >
          <div
            v-show="isOpen"
            class="md:hidden overflow-hidden bg-gray-800"
          >
            <a href="#" class="block px-4 py-2 hover:bg-gray-700">Accueil</a>
            <a href="#" class="block px-4 py-2 hover:bg-gray-700">Services</a>
            <a href="#" class="block px-4 py-2 hover:bg-gray-700">À propos</a>
            <a href="#" class="block px-4 py-2 hover:bg-gray-700">Contact</a>
          </div>
        </transition>
  
      </div>
    </nav>
  </template>
  
  <script>
  export default {
    data() {
      return {
        isOpen: false
      }
    },
    methods: {
      toggleMenu() {
        this.isOpen = !this.isOpen
      }
    }
  }
  </script>