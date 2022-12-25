<template lang="">
    <section id="about">
        <div class="about p-20 px-80 flex flex-col  gap-6" style="scroll-margin-top: 80px;">
            <span class="fancy text-2xl">Over Mij</span>
            <div class="text-xl">
                Mijn naam is Freek van Lier en studeer op dit moment ICT  in de richting Software Engineering aan de Fontys in Eindhoven. 
                Ik ben geïnteresseerd in het ontwikkelen van efficiënte en gebruiksvriendelijke software-oplossingen.
                Verder ben ik altijd op zoek naar manieren om mijn kennis en vaardigheden te verbeteren en ben enthousiast om nieuwe technologieën te leren.

                In mijn vrije tijd hou ik ervan om te werken aan persoonlijke projecten en samen te werken met anderen aan interessante ideeën.
                Ik ben ook actief bezig met het verkennen van nieuwe programmeringstools en frameworks om mijn vaardigheden te verbeteren.
            </div>
        </div>
    </section>
</template>

<script>
export default {
    
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Quicksand:300,500'); /* Custom Font */

.about{
    scroll-margin-top: 80px;
}

.fancy {
    font-family: 'Quicksand', sans-serif;
    display: grid;
    grid-template-columns: 1fr auto 1fr;
    grid-template-rows: 20px 0;
    grid-gap: 20px;
}

.fancy:after,.fancy:before {
  content: " ";
  display: block;
  border-bottom: 1px solid #000000;
} 
</style>