<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import HelloWorld from './components/HelloWorld.vue'
import Navbar from './components/Navbar.vue';
import Footer from './components/Footer.vue';
import Intro from './components/Intro.vue';
import Contact from './components/Contact.vue';
import Projects from './components/Projects.vue';
import TestNav from './components/TestNav.vue';

</script>

<template >

  <TestNav />
  <div class="w-full h-1 bg-gradient-to-r from-cyan-50 to-cyan-50 via-cyan-400"></div>

  <Intro />
  <div class="w-full h-1 bg-gradient-to-r from-cyan-50 to-cyan-50 via-cyan-400"></div>
  <Contact />
  <div class="w-full h-1 bg-gradient-to-r from-cyan-50 to-cyan-50 via-cyan-400"></div>
  <Projects />
  <div class="w-full h-1 bg-gradient-to-r from-cyan-50 to-cyan-50 via-cyan-400"></div>

  <Footer />
</template>
<!--
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

-->