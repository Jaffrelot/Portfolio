<template>
<header>
    <div data-aos="fade-up" class="text-3xl">
        A. Jaffrelot
    </div>
</header>
</template>

<script>
export default {
    name:"Navbar"
}
</script>

<style>

</style>

<div class="absolute top-4 right-4">
    <span class="px-3 py-1 text-white text-xs rounded-full font-semibold">{{ Proj.categorie }}</span>
</div>


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