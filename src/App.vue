<script setup>
import Navbar from './components/Navbar.vue'
import Home from './components/Home.vue'
import Construction from './components/Construction.vue'
</script>

<template>
  <main class="flex flex-col h-screen">
    <Navbar />
    <Home />
  </main>
  <Construction />
</template>

<style>
@import url('https://fonts.googleapis.com/css?family=Quicksand:300,500'); /* Custom Font */

body{
  background-color: rgb(222, 222, 222);
  font-family: 'Quicksand', sans-serif;
}


</style>
