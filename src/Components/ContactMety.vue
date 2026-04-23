<template>
    <section class="relative py-5 overflow-hidden" id="contact">
      <div class="relative max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
  
        <div class="text-center m-16">
          <h2 class="text-4xl md:text-5xl font-bold text-white mb-4">
            Me <span class="text-transparent bg-clip-text bg-gradient-to-r from-blue-400 to-cyan-400">
              contacter
            </span>
          </h2>
          <p class="text-blue-200 text-lg">
            Collaborons ensemble
          </p>
        </div>
  
        <div class="grid lg:grid-cols-2 gap-12">
  
          <!-- INFOS -->
          <div>
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
                  <p class="text-blue-200">Tsaramandroso Fianarantsoa</p>
                </div>
              </div>
            </div>
          </div>
  
          <!-- FORM -->
          <div>
            <form @submit.prevent="sendEmail" class="space-y-6">
  
              <div class="grid sm:grid-cols-2 gap-6">
                <div>
                  <label class="text-white text-sm font-medium mb-2 block">Nom</label>
                  <input
                    v-model="form.name"
                    type="text"
                    class="w-full bg-gray-800/50 border border-blue-500/30 rounded-xl px-4 py-3 text-white"
                  >
                </div>
  
                <div>
                  <label class="text-white text-sm font-medium mb-2 block">Email</label>
                  <input
                    v-model="form.email"
                    type="email"
                    class="w-full bg-gray-800/50 border border-blue-500/30 rounded-xl px-4 py-3 text-white"
                  >
                </div>
              </div>
  
              <div>
                <label class="text-white text-sm font-medium mb-2 block">Sujet</label>
                <input
                  v-model="form.sujet"
                  type="text"
                  class="w-full bg-gray-800/50 border border-blue-500/30 rounded-xl px-4 py-3 text-white"
                >
              </div>
  
              <div>
                <label class="text-white text-sm font-medium mb-2 block">Message</label>
                <textarea
                  v-model="form.message"
                  rows="4"
                  class="w-full bg-gray-800/50 border border-blue-500/30 rounded-xl px-4 py-3 text-white"
                ></textarea>
              </div>
  
              <button
                type="submit"
                :disabled="loading"
                class="w-full bg-gradient-to-r from-blue-500 to-cyan-500 text-white font-semibold py-3 rounded-xl"
              >
                {{ loading ? 'Envoi...' : 'Envoyer' }}
              </button>
  
            </form>
          </div>
  
        </div>
      </div>
    </section>
  </template>
  
  <script setup>
  import { ref } from 'vue'
  import emailjs from '@emailjs/browser'
  import { EnvelopeIcon, MapPinIcon, PhoneIcon } from '@heroicons/vue/16/solid'
  
  const form = ref({
    name: '',
    email: '',
    sujet: '',
    message: ''
  })
  
  const loading = ref(false)
  
  const sendEmail = async () => {
  
    console.log("DATA:", form.value) // DEBUG
  
    if (!form.value.name || !form.value.email || !form.value.message) {
      alert("Champs obligatoires manquants")
      return
    }
  
    loading.value = true
  
    try {
      await emailjs.send(
        'service_m03sioq',
        'template_qxogvfa',
        {
          name: form.value.name,
          email: form.value.email,
          sujet: form.value.sujet,
          message: form.value.message
        },
        'GlVhRxOfYKxjhvMlT'
      )
  
      alert("Message envoyé")
  
      form.value = {
        name: '',
        email: '',
        sujet: '',
        message: ''
      }
  
    } catch (e) {
      console.error(e)
      alert("Erreur ")
    }
  
    loading.value = false
  }
  </script>