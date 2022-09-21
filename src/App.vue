<script setup>
import Navbar from './components/Navbar.vue'
import Home from './components/Home.vue'
import Over from './components/Over.vue'
import Construction from './components/Construction.vue'
import Projects from './components/Projects.vue';

</script>

<template>
    <Navbar />
    <Home />
    <!-- <Over /> -->
    <!-- <Projects /> -->
    <!-- <Construction /> -->
</template>

<style>
@import url('https://fonts.googleapis.com/css?family=Quicksand:300,500'); /* Custom Font */

body{
  background-color: rgb(246, 246, 246);
  font-family: 'Quicksand', sans-serif;
  overflow: overlay;
}

/* Firefox */
* {
  scrollbar-width: thin;
  scrollbar-color: #0000004c;
}

/* Chrome, Edge, and Safari */
::-webkit-scrollbar {
    width: 6px;
}

::-webkit-scrollbar-track {
    background-color: transparent;
}

::-webkit-scrollbar-thumb {
  background-color: #0000004c;
  border-radius: 10px;
  border: 6px solid transparent;
  /* background-clip: content-box; */
}

::-webkit-scrollbar-thumb:hover {
    background-color: #0000007d;
}

</style>
