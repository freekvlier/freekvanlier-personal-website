<template lang="">
    <section id="about">
        <div class="about p-20 px-80 flex flex-col  gap-6" style="scroll-margin-top: 80px;">
            <span class="fancy text-2xl">Over Mij</span>
            <div class="text-xl">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
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