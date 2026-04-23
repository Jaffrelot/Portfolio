<template>
  <section class="relative py-5 overflow-hidden" id="contact">
    <div class="relative max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center m-16" data-aos="fade-up">
            <h2 class="text-4xl md:text-5xl font-bold text-white mb-4">
                Me <span class="text-transparent bg-clip-text bg-linear-to-r from blue-400 to-cyan-400">
                    contacter
                </span>
            </h2>
            <p class="text-blue-200 text-lg">
                Collaborons ensemble
            </p>
        </div>

        <div class="grid lg:grid-cols-2 gap-12">
            <!-- Contact info -->
            <div data-aos="fade-right">
                <h3 class="text-2xl font-bold text-white mb-6 md:text-center">
                    Coordonnées
                </h3>
                <div class="space-y-6">
                    <div class="flex items-center gap-4">
                        <EnvelopeIcon class="w-6 h-6 text-blue-400"/>
                        <div>
                            <p class="text-white font-semibold">Email</p>
                            <p class="text-blue-200">andriatsitohainarivo7@gmail.com</p>
                        </div>
                    </div>
                    <div class="flex items-center gap-4">
                        <PhoneIcon class="w-6 h-6 text-blue-400"/>
                        <div>
                            <p class="text-white font-semibold">Téléphone</p>
                            <p class="text-blue-200">+261 38 86 666 49</p>
                        </div>
                    </div>
                    <div class="flex items-center gap-4">
                        <MapPinIcon class="w-6 h-6 text-blue-400"/>
                        <div>
                            <p class="text-white font-semibold">Localisation</p>
                            <p class="text-blue-200">Tsaramandroso FIANARANTSOA</p>
                        </div>
                    </div>
                </div>
                <!-- Contact par internet -->
                 <div class="mt-8">
                    <h4 class="text-lg font-bold text-white mb-4">
                        Suivez-moi
                    </h4>
                    <div class="flex gap-4">
                        <a href="#" class="p-3 bg-cyan-500/20 border border-cyan-400/30 rounded-xl text-blue-400 hover:bg-blue-500/30 transition-all">
                            icone
                        </a>
                        <a href="#" class="p-3 bg-cyan-500/20 border border-cyan-400/30 rounded-xl text-pink-400 hover:bg-blue-500/30 transition-all">
                            icone
                        </a>
                    </div>
                 </div>
            </div>
            <!-- Contact formulaire -->
            <div data-aos="fade-left">
                <form action="" class="space-y-6">
                    <div class="grid sm:grid-cols-2 gap-6">
                        <div>
                            
                            <label for="" class="text-white text-sm font-medium mb-2 block">
                                Nom
                            </label>
                            <input type="text" class="w-full bg-gray-800/50 border border-blue-500/30 rounded-xl px-4 py-3 text-white placeholder-blue-300 focus:border-blue-400 focus:outline-none transition-all">
                            
                        </div>
                        <div>
                            
                            <label for="" class="text-white text-sm font-medium mb-2 block">
                                Email
                            </label>
                            <input type="email" class="w-full bg-gray-800/50 border border-blue-500/30 rounded-xl px-4 py-3 text-white placeholder-blue-300 focus:border-blue-400 focus:outline-none transition-all">
                            
                        </div>
                    </div>
                       
                        <div>
                            
                            <label for="" class="text-white text-sm font-medium mb-2 block">
                                Sujet
                            </label>
                            <input type="text" class="w-full bg-gray-800/50 border border-blue-500/30 rounded-xl px-4 py-3 text-white placeholder-blue-300 focus:border-blue-400 focus:outline-none transition-all">
                            
                        </div>
                        <div>
                            
                            <label for="" class="text-white text-sm font-medium mb-2 block">
                                Message
                            </label>
                            
                            <textarea rows="4" class="w-full bg-gray-800/50 border border-blue-500/30 rounded-xl px-4 py-3 text-white placeholder-blue-300 focus:border-blue-400 focus:outline-none transition-all">

                            </textarea>
                        </div>
                        <button type="submit" class=" w-full bg-linear-to-r from-blue-500 to-cyan-500 text-white font-semibold py-3 rounded-xl hover:shadow-lg hover:shadow-blue-500/25 transition-all duration-300">
                            Envoyer
                        </button>
                    
                </form>
            </div>
        </div>
    </div>
  </section>
</template>

<script setup>
import { EnvelopeIcon,MapPinIcon,PhoneIcon } from '@heroicons/vue/16/solid';

</script>

<style>

</style>