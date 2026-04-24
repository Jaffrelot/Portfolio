<template>
  
<section>
    <div class="max-w-7xl mx-auto px-4 text-white sm:px-6 lg:px-8">
        <div class="text-center m-16" data-aos="fade-up">
            <h2 class="text-4xl md:text-5xl font-bold text-white mb-4">
                Mes <span class="text-transparent bg-clip-text bg-linear-to-r from-blue-400 to-cyan-400">
                        Services
                    </span>  
            </h2>
            <p class="text-lg max-w-2xl mx-auto" data-aos="fade-up" data-aos-delay="100">
                Je conçois des solutions digitales modernes pour répondre à vos besoins.
            </p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
            <div class="group relative p-8 rounded-2xl bg-linear-to-br from-gray-800/50 to-blue-900/30 backdrop-blur-sm border border-blue-500/20 hover:border-blue-400/40 transition-all duration-500 hover:transform hover:-translate-y-2" v-for="(service,index) in Services" :key="service.id" :data-aos="'fade-up'" :data-aos-delay="(index * 100) + 200">
                <div class="absolute inset-0 bg-linear-to-r from-blue-500/5 to-cyan-500/5 rounded-2xl opacity-0 duration-500 group-hover:opacity-100 transition-opacity">
                </div>
                <div class="relative mb-6">
                    <div class="inline-flex items-center justify-center w-16 h-16 rounded-xl bg-linear-to-r from-blue-500/20 to-cyan-500/20 border-blue-400/30 group-hover:scale-110 transition-transform duration-300">
                        <component :is="service.icon" class="w-8 h-8 text-blue-400">
                        </component>  
                    </div>
                </div>
                <div class="relative">
                    <h3 class="text-xl font-bold text-white mb-3 group-hover:text-blue-400 transition-colors duration-300">
                        {{ service.titre }}
                    </h3>
                    <p class="text-blue-100 leading-relaxed">
                        {{ service.desc }}
                    </p>
                </div>
                <div class="absolute bottom-6 right-6 opacity-0 group-hover:opacity-100 transform translate-x-4 group-hover:translate-x-0 transition-all duration-300">
                <ArrowRightIcon class="w-6 h-6 text-cyan-400"/>
                </div>
            </div>
        </div>
    </div>
</section>


</template>
    
    <script setup>
import { ArrowRightIcon,CodeBracketIcon, DevicePhoneMobileIcon, PaintBrushIcon } from '@heroicons/vue/16/solid';
import { ref } from 'vue';

    
const Services = ref([
{
    id:1,
    icon:CodeBracketIcon,
    titre:"Developpement Web",
    desc:"Je réalise des sites web et des applications performantes, sécurisées et evolutive.Que ce soit pour un site vitrine,une plateforme ou une application métier,je m'adapte à vos besoins pour proposer une solution fiable et moderne.",
},
{
    id:2,
    icon:DevicePhoneMobileIcon,
    titre:"Developpement Mobile",
    desc:"Je développe des applications mobiles intuitives et accessibles,conçues pour offrir une expérience fluide.",
},
{
    id:3,
    icon:PaintBrushIcon,
    titre:"UI/UX Design",
    desc:"Je conçois des interfaces modernes, esthetiques et ergonomique. L'objectif est de garantir une navigation simple,agréable et adaptée aux utilisateurs finaux.",
},



])


  
    
    
    </script>
    
    <style>
    
    </style>