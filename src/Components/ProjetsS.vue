<template>
    <section>
        <div class="text-center mb-16" data-aos="fade-up">
            <h2 class="text-4xl md:text-5xl font-bold text-white mb-4">
                Mes
                <span class="text-transparent bg-clip-text bg-linear-to-r from-blue-400 to-cyan-400">Projets</span> 
            </h2>
            <p class="text-blue-200 text-lg max-w-2xl mx-auto">
                Collection des projets que j'ai realisé pendant mes formations universitaire et stage
            </p>
        </div>

         <!-- Grid -->
          <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">

            <div v-for="(Proj,index) in Projets" :key="Proj.id" data-aos="fade-up" :data-aos-delay="(index + 1) * 100" class="group relative bg-linear-to-br from-gray-800/50 to-blue-900/30 rounded-3xl overflow-hidden border backdrop-blur-sm hover:border-blue-400/40 transition-all duration-500 hover:transform hover:-translate-y-2">
            <!-- image -->
            <div class="relative overflow-hidden">
                <img :src="Proj.image" :alt="Proj.titre" class="w-full h-50 object-cover group-hover:scale-110 transition-transform duration-500">
                

                <div class="absolute inset-0 bg-linear-to-t from-gray-900 via-transparent to-transparent"></div>
                <div class="absolute top-4 right-4">
                    <span class="px-3 py-1 text-white text-xs rounded-full font-semibold" :class="Proj.BadgeCouleur">{{ Proj.categorie }}</span>
                </div>
                
            </div>

            <!-- Contenu du projet -->
            <div class="p-6">
                <h3 class="text-xl font-bold text-white">{{ Proj.titre }}</h3>
                <p class="text-blue-100 text-sm leading-relaxed mb-4">{{ Proj.descr }}</p>

                    <!-- technologie -->
                <div class="flex flex-wrap gap-2 mb-4">
                    <span v-for="technologies in Proj.technologie" :key="technologies" class="px-2 py-1 border rounded text-xs" :class="technologies.class">
                        {{ technologies.nom }}
                    </span>
                </div>

            </div>



        </div>


          </div>
        
        </section>
    </template>
    
    <script setup>
import { ref } from 'vue';

    
const Projets = ref([
{
    id:1,
    titre:"Projet 1",
    descr:"Lorem ipsum dolor sit amet consectetur, adipisicing elit. Necessitatibus ipsa, voluptatum quidem qui quis assumenda veritatis voluptate nihil minus! Quasi ipsam eum libero accusantium impedit culpa consequatur nesciunt itaque quod.",
    image:"../public/pexels-photo-4073043.jpeg",
    categorie:"Fullstack",
    BadgeCouleur:"bg-blue-500",
    technologie:[{
        nom:"Vuejs",
        class:'bg-blue-500/20 border-blue-400/30 text-blue-200'},
    {
        nom:"React",
        class:"bg-cyan-500/20 border-cyan-400/30 text-cyan-200"
    },

], 
},
{
    id:2,
    titre:"Projet 2",
    descr:"Lorem ipsum dolor sit amet consectetur, adipisicing elit. Necessitatibus ipsa, voluptatum quidem qui quis assumenda veritatis voluptate nihil minus! Quasi ipsam eum libero accusantium impedit culpa consequatur nesciunt itaque quod.",
    image:"../public/Copilot_20251217_111254.png",
    categorie:"Backend",
    BadgeCouleur:"bg-cyan-500",
    technologie:[{
        nom:"Tailwindcss",
        class:'bg-blue-500/20 border-blue-400/30 text-blue-200'
    },
    {
        nom:"React",
        class:'bg-cyan-500/20 border-cyan-400/30 text-cyan-200'
    },
    {
        nom:"Nodejs",
        class:'bg-cyan-500/20 border-cyan-400/30 text-cyan-200'
    }
] 
},

{
    id:3,
    titre:"Portfolio App",
    descr:"Lorem ipsum dolor sit amet consectetur, adipisicing elit. Necessitatibus ipsa, voluptatum quidem qui quis assumenda veritatis voluptate nihil minus! Quasi ipsam eum libero accusantium impedit culpa consequatur nesciunt itaque quod.",
    image:"../public/football.jpeg",
    categorie:"Frontend",
    BadgeCouleur:"bg-cyan-700",
    technologie:[{
        nom:"Vuejs",
        class:'bg-blue-500/20 border-blue-400/30 text-blue-200'
    },
    {
        nom:"Tailwind CSS",
        class:'bg-cyan-500/20 border-cyan-400/30 text-cyan-200'
    },
    {
        nom:"AOS",
        class:'bg-cyan-200/20 border-cyan-400/30 text-cyan-200'
    }
] 
}


])


  
    
    
    </script>
    
    <style>
    
    </style>