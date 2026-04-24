<template>
  <section class="relative w-full overflow-hidden min-h-screen flex items-center">
    
    <div class="w-full px-5 sm:px-8 md:px-12 lg:px-8 max-w-5xl lg:max-w-7xl mx-auto">
        
        <div class="grid lg:grid-cols-2 gap-10 xl:gap-14 items-center">
            <div class="flex flex-col md:mt-0 mt-20 justify-center">
             <div class="text-white lg:text-left" data-aos="fade-right">
                <h1 class="text-white font-bold md:text-4xl lg:text-5xl text-3xl leading-tight">
                    Bonjour, Je m'appelle <span class="text-transparent bg-clip-text bg-linear-to-r from-blue-400 to-cyan-400">ANDRIATSITOHAINARIVO Jaffrelot Bizoux Abrivard</span>
                </h1>
            <!-- description -->
            <p class="text-blue-200 font-medium text-lg md:text-xl mt-4" data-aos="fade-right" data-aos-delay="100">
                Développeur Full-Stack
            </p>
        </div>
        
         <p class="text-gray-300 pt-6 max-w-xl text-center lg:text-left mx-auto text-lg leading-relaxed" data-aos="fade-right" data-aos-delay="200">
            Passionné par le monde informatique, je souhaite mettre mes compétences en développement au service d’une entreprise.</p>

         <!-- bouton cv et contacter -->
          <div class="flex flex-col pt-8 gap-4 sm:flex-row sm:mx-auto sm:w-max lg:mx-0" data-aos="fade-up" data-aos-delay="300">
            
            <!-- 1er button -->
            <a href="#contact" class="px-8 py-4 rounded-xl relative group w-full flex justify-center overflow-hidden sm:w-max bg-linear-to-r from-blue-600 to-cyan-600 hover:from-blue-500 transition-all duration-300">
                <span class="relative flex items-center text-white font-semibold text-lg">
                    Contactez-moi
                    <ArrowRightIcon class="ml-2 w-5 h-5 group-hover:translate-x-1 transition-transform"/>
                </span>
            </a>

            <!-- 2eme button -->
            <a href="/public/CV_ANDRIATSITOHAINARIVO_Jaffrelot.pdf" download="CV_Jaffrelot.pdf" class="border-2 text-blue-400 border-blue-400 group px-8 py-4 rounded-xl w-full sm:w-max hover:bg-blue-400/10 transition-all duration-300">
                <div class="flex items-center justify-center relative">

                    <ArrowDownTrayIcon class="w-5 h-5 group-hover:translate-y-1 transition-transform"/>
                    <span class="pl-3 font-semibold text-lg">Télécharger le CV</span>

                </div>
                 
            </a>  
          </div>

<div class="flex items-center justify-center lg:justify-start gap-8 pt-12">
    <div class="text-center">
        <div class="text-2xl font-bold text-blue-400">50+</div>
        <div class="text-blue-200 text-sm">Projets</div>
    </div>
    <div class="text-center">
        <div class="text-2xl font-bold text-blue-400">50+</div>
        <div class="text-blue-200 text-sm">Projets</div>
    </div>
    <div class="text-center">
        <div class="text-2xl font-bold text-blue-400">50+</div>
        <div class="text-blue-200 text-sm">Projets</div>
    </div>
</div>

        </div>

          <!-- IMAGE -->
          <div class="lg:h-full flex justify-center lg:justify-end">
            <div class="relative w-full max-w-md lg:max-w-lg">
                <div class="bg-linear-to-r from-blue-400 to-cyan-600 rounded-[50%_40%_30%_10%/60%_30%_70%_30%] backdrop-blur-sm shadow-2xl border border-blue-500/30 -translate-y-6" data-aos="zoom-in">
                    <div class="rounded-xl overflow-hidden">
                        <img src="/public/Hero.png" alt="Jaffrelot - Full Stack Developer" srcset="" class="object-contain">
                    </div>
                    
                </div>
                
            </div>
          </div>
    </div>
    </div>



  </section>
</template>

<script setup>
import { ArrowRightIcon,ArrowDownTrayIcon } from '@heroicons/vue/16/solid';
</script>

<style>

</style>