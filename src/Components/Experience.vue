<template>
  <section class="relative py-20 overflow-hidden" id="expérience">

    <div class="relative max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16" data-aos="fade-up">
            <h2 class="text-4xl md:text-5xl font-bold text-white mb-4">
                <span class="text-transparent bg-clip-text bg-linear-to-r from-blue-400 to-cyan-400">
                    Compétences
                </span>& Experience
            </h2>
            <p class="text-blue-200 text-lg max-w-2xl mx-auto">
                Mes compétences techniques et mon expérience professionelle
            </p>
        </div>
        <div class="grid lg:grid-cols-2 gap-12 lg:gap-16">
                <div data-aos="fade-right">
                    <h3 class="text-2xl font-bold text-white mb-8 flex items-center gap-3">
                        Compétences techniques
                    </h3>
                    <div class="space-y-6">
                        <div v-for="skill in skills" :key="skill.id" class="group">
                            <div class="flex items-center justify-between mb-3">
                                <span class="text-blue-200 font-semibold flex items-center gap-2">

                                <component :is="skill.icon" class="w-9 h-9" :class="skill.iconColor">
                                        
                                </component>    
                                <span>
                                    {{ skill.titre }}
                                </span>
                                
                                </span>
                                
                                <span :class="skill.pourcentageColor">
                                    {{ skill.pourcentage }} %
                                </span>
                            </div>

                            <div class="h-2 bg-gray-700 rounded-full overflow-hidden">
                                <div class="h-full rounded-full transition-all duration-100 group-hover:scale-105" :class="skill.gradient" :style="{width: skill.pourcentage + '%'}">
                                     
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="mt-12">
                        <h4 class="text-xl font-bold text-white mb-6 flex items-center gap-2">
                            <Squares2X2Icon class="w-6 h-6 text-cyan-400"/>
                            Technologies utilisées 
                        </h4>
                        <div class="flex flex-wrap gap-3">
                            <span v-for="tech in techStack" :key="tech" class="px-4 py-2 bg-linear-to-r from-blue-500/20 border border-blue-400/30 rounded-full text-blue-200 text-sm font-medium hover:scale-105 transition-transform duration-300">
                                {{ tech }}
                            </span>
                        </div>
                    </div>
                    <div class="mt-12">
                        <h4 class="text-xl font-bold text-white mb-6 flex items-center gap-2">
                            <CogIcon class="w-6 h-6 text-cyan-400"/>
                            Outils et Design utilisées 
                        </h4>
                        <div class="flex flex-wrap gap-3">
                            <span v-for="outD in outilDesign" :key="outD" class="px-4 py-2 bg-linear-to-r from-blue-500/20 border border-blue-400/30 rounded-full text-blue-200 text-sm font-medium hover:scale-105 transition-transform duration-300">
                                {{ outD }}
                            </span>
                        </div>
                    </div>
                </div>

                <div data-aos="fade-left">
                    <h3 class="text-2xl font-bold text-white mb-8 flex items-center gap-2">
                        <BriefcaseIcon class="w-8 h-8 text-cyan-400"/>
                        Expérience professionnelle
                    </h3>
                    <div class="space-y-8">
                        <div v-for="exp in experiences" :key="exp.id" class="relative pl-8 border-l-2 group" :class="exp.borderColor">
                            <div class="absolute -left-2 top-0 w-4 h-4 rounded-full group-hover:scale-150 transition-transform duration-300" :class="exp.dotColor"></div>
                            <div class="bg-linear-to-br from-gray-800/50 to-blue-900/30 rounded-2xl p-6 border backdrop-blur-sm group-hover:border-blue-400/20 hover:scale-105 transition-all duration-300" :class="exp.borderClass">
                                <div class="flex flex-col sm:flex-row sm:items-center sm:justify-between mb-3">
                                    <h4 class="text-lg font-bold text-white">
                                        {{ exp.position }}
                                    </h4>
                                    <span :class="exp.dateColor" class="mt-1 sm:mt-0">
                                        {{ exp.Periode }}
                                    </span>
                                </div>
                                
                                <p :class="exp.EntrepriseColor" class="font-medium mb-3">
                                  {{ exp.Entreprise }}  
                                </p>
                                <p class="text-blue-100 text-sm leading-relaxed">
                                    {{ exp.desc }}
                                </p>

                            </div>
                        </div>
                    </div>

                </div>



            </div>
    </div>
    
  </section>
</template>

<script setup>
import { CodeBracketIcon, DevicePhoneMobileIcon, PaintBrushIcon, ServerIcon,Squares2X2Icon,BriefcaseIcon,CogIcon } from '@heroicons/vue/16/solid';  
const skills = [
    {
        id:1,
        titre:"Developpement Frontend",
        icon:CodeBracketIcon,
        iconColor:"text-blue-400",
        pourcentage:80,
        pourcentageColor:"text-blue-400 text-sm",
        gradient:"bg-linear-to-r from-blue-500 to-cyan-500",
    },
    {
        id:2,
        titre:"Développement Backend",
        icon:ServerIcon,
        iconColor:"text-blue-400",
        pourcentage:85,
        pourcentageColor:"text-blue-400 text-sm",
        gradient:"bg-linear-to-r from-blue-500 to-cyan-500",
    },
    {
        id:3,
        titre:"Développement mobile",
        icon:DevicePhoneMobileIcon,
        iconColor:"text-blue-400",
        pourcentage:50,
        pourcentageColor:"text-blue-400 text-sm",
        gradient:"bg-linear-to-r from-blue-500 to-cyan-500",
    },
    {
        id:4,
        titre:"UI/UX Design",
        icon:PaintBrushIcon,
        iconColor:"text-blue-400",
        pourcentage:50,
        pourcentageColor:"text-blue-400 text-sm",
        gradient:"bg-linear-to-r from-blue-500 to-cyan-500",
    },


]

const techStack = [
    'Vue.js','Tailwind css','Bootstrap','Node.js','Express.js','MySQL','PosgreSQL','PHP','Supabase','HTML','CSS','Javascript'
]
const outilDesign = [
    'VS Code','Git','Figma','Postman','GanttProject',"Win'Design"
]


const experiences = [
    {
        id:1,
        position:"Développeur Full-Stack",
        Entreprise:"EC TRAVAUX",
        Periode:"2024 - 2025",
        desc:"Développement d’une plateforme web de chiffrage automatisé des projets de construction intégrant l’intelligence artificielle",
        borderColor:"border-blue-500/30",
        dotColor:"bg-blue-500",
        borderClass:"border-blue-500/20",
        dateColor:"text-blue-400 text-sm font-semibold",
        EntrepriseColor:"text-cyan-400",
    },
    {
        id:2,
        position:"Développeur Backend",
        Entreprise:"ENI (Ecole Nationale d'Informatique)",
        Periode:"2023 - 2024",
        desc:"Réalisation d’une application web pour l’approvisionnement de stock en Vue.js et Node.js",
        borderColor:"border-blue-500/30",
        dotColor:"bg-blue-500",
        borderClass:"border-blue-500/20",
        dateColor:"text-blue-400 text-sm font-semibold",
        EntrepriseColor:"text-cyan-400",
    },
    {
        id:3,
        position:"Développeur Full-Stack",
        Entreprise:"DGI (Direction Générale de l'Impôt)",
        Periode:"2022 - 2023",
        desc:"Développement d’un module pour une solution RPA de Télépaiement en matière ISI",
        borderColor:"border-blue-500/30",
        dotColor:"bg-blue-500",
        borderClass:"border-blue-500/20",
        dateColor:"text-blue-400 text-sm font-semibold",
        EntrepriseColor:"text-cyan-400",
    },
    {
        id:4,
        position:"Développeur Backend",
        Entreprise:"WBS (World Business Solution)",
        Periode:"2021 - 2022",
        desc:"Conception et Réalisation d’une application web pour la gestion de l’enseignant en Vue.js et Laravel",
        borderColor:"border-blue-500/30",
        dotColor:"bg-blue-500",
        borderClass:"border-blue-500/20",
        dateColor:"text-blue-400 text-sm font-semibold",
        EntrepriseColor:"text-cyan-400",
    },
    
]



</script>

<style>

</style>