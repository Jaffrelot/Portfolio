<template>
    
    <button
      @click="toggleDark"
      class="p-2 rounded-full transition-colors duration-300
             hover:bg-gray-300
             dark:bg-gray-700 dark:hover:bg-gray-600"
      :aria-label="isDark ? 'Activer le mode clair' : 'Activer le mode sombre'"
    >
      <!-- Lune (mode clair actif) -->
      <svg v-if="!isDark" class="h-5 w-5 text-gray-800" fill="none"
        viewBox="0 0 24 24" stroke="currentColor">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
          d="M21 12.79A9 9 0 1111.21 3 7 7 0 0021 12.79z" />
      </svg>
      <!-- Soleil (mode sombre actif) -->
      <svg v-else class="h-5 w-5 text-yellow-300" fill="none"
        viewBox="0 0 24 24" stroke="currentColor">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
          d="M12 3v1m0 16v1m9-9h-1M4 12H3m15.364-6.364l-.707.707M6.343 17.657l-.707.707
             M17.657 17.657l-.707-.707M6.343 6.343l-.707-.707M12 8a4 4 0 100 8 4 4 0 000-8z" />
      </svg>
    </button>
  </template>
  
  <script setup>
  import { useDarkMode } from './useDarkMode'
  const { isDark, toggleDark } = useDarkMode()
  
  </script>