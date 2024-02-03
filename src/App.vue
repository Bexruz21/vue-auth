<script setup>
import Navbar from './components/Navbar.vue';

</script>

<template>
  <Navbar />
  <section class="section">
    <RouterView />
  </section>
</template>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  text-decoration: none;
  font-family: Arial, Helvetica, sans-serif;
}
body {
  min-height: 100vh;
  background-color: #1c1c1c;
}
</style>

