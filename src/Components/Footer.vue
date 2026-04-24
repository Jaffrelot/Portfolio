<template>
  <footer class="relative bg-gray-900/80 border-t border-blue-500/20">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 py-12">
        <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
            <!-- Brand -->
             <div class="md:col-span-2">
                <div class="text-2xl font-bold bg-linear-to-r from-blue-400 to-cyan-400 bg-clip-text text-transparent mb-4">
                    A. Jaffrelot Bizoux Abrivard
                </div>
                <p class="text-blue-200 text-sm leading-relaxed max-w-md">
                    Passionné par le développement web, je crée des solutions modernes adaptées aux besoins des utilisateurs.
                </p>
                <div class="flex gap-4 mt-6">
                    <a href="#" class="p-2 bg-blue-500/20 border border-blue-400/30 rounded-lg text-blue-400 hover:bg-blue-500/30 transition-all">
                        <EnvelopeIcon class="w-5 h-5"/>
                    </a>
                    <a href="#" class="p-2 bg-blue-400/20 border border-blue-400/30 rounded-lg text-blue-400 hover:bg-blue-500/30 transition-all">
                        <PhoneIcon class="w-5 h-5"/>
                    </a>
                    <a href="#" class="p-2 bg-blue-400/20 border border-blue-400/30 rounded-lg text-blue-400 hover:bg-blue-500/30 transition-all">
                        <MapPinIcon class="w-5 h-5"/>
                    </a>
                </div>
             </div>
             
             <!-- Lien rapide -->
             <div>
                <h3 class="text-white font-semibold mb-4">
                    Lien rapide
                </h3>
                <ul class="space-y-2">
                    <li v-for="liens in lienRapide" :key="liens.name">
                        <a :href="liens.href" class="text-blue-200 hover:text-blue-400 text-sm transition-colors">
                            {{ liens.name }}
                        </a>
                    </li>
                </ul>
             </div>
             <!-- Services -->
             <div>
                <h3 class="text-white font-semibold mb-4">
                    Services
                </h3>
                <ul class="space-y-2">
                    <li v-for="service in services" :key="service">
                        <a href="#" class="text-blue-200 hover:text-blue-400 text-sm transition-colors">
                            {{ service }}
                        </a>
                    </li>
                </ul>
             </div>
        </div>

        <!-- bottom bar -->
        <div class="border-t border-blue-500/20 mt-8 pt-8 flex flex-col md:flex-row justify-between items-center">
                <p class="text-blue-300 text-sm">
                    @ {{ AnneeActuel }} Jaffrelot. Tous droits réservés
                </p>
                <div class="flex gap-6 mt-4 md:mt-0">
                    <a href="#" class="text-blue-400 text-sm transition-colors">
                        Politique de confidentialité
                    </a>
                    <a href="#" class="text-blue-400 text-sm transition-colors">
                        Condition d'utilisation
                    </a>
                </div>
             </div>
    </div>
  </footer>
</template>

<script setup>
import { EnvelopeIcon,MapPinIcon,PhoneIcon } from '@heroicons/vue/16/solid';
const AnneeActuel = new Date().getFullYear()
const lienRapide = [
    {name: 'Accueil',href: '#accueil'},
    {name: 'Compétence',href: '#expérience'},
    {name: 'Projets',href: '#projets'},
    {name: 'Expérience',href: '#expérience'},
    {name: 'Contact',href: '#contact'},
]
const services = [
    'Developpement web',
    'Developpement Mobile',
    'UI/UX Design'

]

</script>

<style>

</style>