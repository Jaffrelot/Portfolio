<template>
    
  <button
    @click="toggleDark"
    class="relative w-10 h-10 rounded-full flex items-center justify-center
           bg-gray-100 hover:bg-gray-200
           dark:bg-white/10 dark:hover:bg-white/20
           border border-gray-200 dark:border-white/10
           transition-all duration-300"
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

import { ref, onMounted, watch } from 'vue'

const isDark = ref(false)

export function useDarkMode() {

  onMounted(() => {
    const saved = localStorage.getItem('theme')

    if (
      saved === 'dark' ||
      (!saved && window.matchMedia('(prefers-color-scheme: dark)').matches)
    ) {
      isDark.value = true
    }
  })

  watch(isDark, (newValue) => {
    if (newValue) {
      document.documentElement.classList.add('dark')
      localStorage.setItem('theme', 'dark')
    } else {
      document.documentElement.classList.remove('dark')
      localStorage.setItem('theme', 'light')
    }
  }, { immediate: true })

  const toggleDark = () => {
    isDark.value = !isDark.value
  }

  return { isDark, toggleDark }
}

</script>