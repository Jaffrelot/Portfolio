<template>
  <section class="min-h-screen w-full overflow-hidden flex items-center">
    
    <div class="text-white px-5 max-w-5xl" data-aos="fade-right">
        
        <h1 class="text-white font-bold text-4xl leading-tight">
            Bonjour, je m'appelle <span class="text-transparent bg-clip-text bg-linear-to-r from-blue-400 to-cyan-400">ANDRIATSITOHAINARIVO Jaffrelot Bizoux Abrivard</span>
        </h1>
        <!-- description -->
         <p class="text-blue-200 font-medium text-lg mt-4" data-aos="fade-right">
            Développeur Full-Stack
         </p>
         <p class="text-gray-300 pt-6 max-w-xl text-lg leading-relaxed">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Quas vitae sequi minima quasi, modi reprehenderit enim ullam esse, nemo assumenda autem. Reprehenderit, dicta tempore.
         </p>

         <!-- bouton cv et contacter -->
          <div class="flex flex-col pt-8 gap-4 sm:flex-row sm:mx-auto">
            
            <!-- 1er button -->
            <button class="px-8 py-4 rounded-xl w-full sm:w-max bg-linear-to-r from-blue-600 to-cyan-600 hover:from-blue-500 transition-all duration-300">
                <span class="text-white font-semibold text-lg">Contact Me</span>
            </button>

            <!-- 2eme button -->
            <button class="border-2 text-blue-400 border-blue-400 px-8 py-4 rounded-xl w-full sm:w-max hover:bg-blue-400/10 transition-all duration-300">
                <span class="font-semibold text-lg">Download CV</span>
                 
            </button>

            
          </div>

          <!-- IMAGE -->
          <div class="flex justify-center">
            <div class="w-full max-w-md overflow-hidden">
                <img src="/public/Abrivard.jpg" alt="Jaffrelot - Full Stack Developer" srcset="" class="w-[500px] h-[500px] object-contain">
            </div>
          </div>

    </div>
  </section>
</template>

<script>
export default {

}
</script>

<style>

</style>