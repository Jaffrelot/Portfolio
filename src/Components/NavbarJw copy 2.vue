<template>
  
<div>
    <button class="bg-blue-500 px-5 py-2" @click="toogleMenu">Afficher/cacher</button>
    <p :class="isVisible ? 'block' : 'hidden'">Bonjour ! je suis visible</p>
</div>

</template>

<script>
export default {
    name:"NavbarJw",
    data(){
        return{
            isVisible:false
        }
    },
    methods:{
        toogleMenu(){
            this.isVisible = !this.isVisible;
        }
    }
}
</script>

<style>

</style>