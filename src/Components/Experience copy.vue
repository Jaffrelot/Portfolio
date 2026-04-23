<template>
  <section class="py-20">
    <div class="text-center" data-aos="fade-up">
        <h2>
            Experience
        </h2>
        <div class="space-y-8">
        <div class="relative pl-8 border-b group" :class="exp.borderColor" v-for="exp in experiences" :key="exp.id">
            <div class="absolute -left-2 top-0 w-4 h-4 rounded-full group-hover:scale-150 transition-transform duration-300" :class="exp.dotColor">
                <div class="bg-linear-to-br from-gray-800/50 to-blue-900/30 rounded-2xl p-6 border backdrop-blur-sm group-hover:border-blue-400/40 transition-all duration-300" :class="exp.borderClass">
                    <div class="flex flex-col sm:flex-row sm:items-center sm:justify-between mb-3">
                        <h4>{{ exp.position }}</h4>
                    </div>
                </div>
            </div>
        </div>
    </div>
    </div>
    
  </section>
</template>

<script setup>

const experiences = [
    {
        id:1,
        position:"Senior",
        Entreprise:"EC TRAVAUX",
        Periode:"2025",
        desc:"Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ea, eius. Consequatur, temporibus qui, tempore eius repellat, quas quaerat dolore sed laboriosam facere quam provident! Suscipit quia ipsum dolorum accusantium qui?",
        borderColor:"border-blue-500/30",
        dotColor:"bg-blue-500",
        borderClass:"bg-blue-500/20",
        dateColor:"text-blue-400 text-sm font-semibold",
        EntrepriseColor:"text-cyan-400",
    },
    {
        id:2,
        position:"junior",
        Entreprise:"EC TRAVAUX",
        Periode:"2025",
        desc:"Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ea, eius. Consequatur, temporibus qui, tempore eius repellat, quas quaerat dolore sed laboriosam facere quam provident! Suscipit quia ipsum dolorum accusantium qui?",
        borderColor:"border-blue-500/30",
        dotColor:"bg-blue-500",
        borderClass:"bg-blue-500/20",
        dateColor:"text-blue-400 text-sm font-semibold",
        EntrepriseColor:"text-cyan-400",
    },
]


</script>

<style>

</style>