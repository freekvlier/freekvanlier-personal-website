<template lang="">
    <div class="about p-20 px-80 flex flex-col  gap-6" style="scroll-margin-top: 80px;">
        <span class="fancy text-2xl">Projecten</span>
        <div class="container mx-auto px-4">
            <div class="flex flex-wrap justify-center">
                <div class="w-1/3 p-4" v-for="project in projects" :key="project.id">
                    <div class="project shadow-lg rounded-lg overflow-hidden">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/66/SMPTE_Color_Bars.svg/1200px-SMPTE_Color_Bars.svg.png" alt="Project afbeelding" class="w-full h-48 object-cover">
                    <div class="px-6 py-4">
                        <h2 class="text-xl font-bold mb-2">{{ project.title }}</h2>
                        <p class="mb-4">{{ project.description }}</p>
                        <a :href="project.url" class="btn btn-blue">Bekijk project</a>
                    </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>


<script>
export default {
  name: 'Projects',
  data() {
    return {
      projects: [
        {
          id: 1,
          title: 'Project 1',
          description: 'Een korte omschrijving van het project',
          url: '/project/1'
        },
        {
          id: 2,
          title: 'Project 2',
          description: 'Een korte omschrijving van het project',
          url: '/project/2'
        }
      ]
    }
  }
}
</script>


<style lang="">
    
</style>