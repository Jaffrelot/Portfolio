<template>
    <button v-if="isVisible" @click="glisserVersHaut" class="fixed bottom-4 right-4 bg-linear-to-r from-blue-600 to-cyan-600 text-white rounded-full w-12 h-12 items-center justify-center text-xl cursor-pointer transition-opacity duration-opacity duration-300 hover:bg-blue-600 hover:scale-110 transition-transform duration-300">
        <div class="flex justify-center">
            <ArrowUpCircleIcon class="w-6 h-6 text-blue-200"/>
        </div>    
    </button>
</template>

<script setup>
import { ArrowUpCircleIcon } from '@heroicons/vue/16/solid';
import { onMounted, onUnmounted, ref } from 'vue';

const isVisible = ref(false);
const handleScroll = () =>{
    isVisible.value = window.scrollY > 300;
}
const glisserVersHaut = () =>{
    window.scrollTo({top:0,behavior:'smooth'})
}
onMounted(() =>{
    window.addEventListener('scroll',handleScroll)
});
onUnmounted(() =>{
    window.removeEventListener('scroll',handleScroll)
});


</script>

<style>

</style>