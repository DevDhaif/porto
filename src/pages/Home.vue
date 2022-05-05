<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import HelloWorld from '../components/HelloWorld.vue'
import Navbar from '../components/Navbar.vue';
import Footer from '../components/Footer.vue';
import Intro from '../components/Intro.vue';
import Contact from '../components/Contact.vue';
import Projects from '../components/Projects.vue';

</script>
<template>
    <div class="mt-12">
        <Intro />
        <div
            class="w-full h-1 bg-gradient-to-r dark:from-cyan-50 from-cyan-800 dark:to-cyan-50 to-cyan-800 via-cyan-300 dark:via-cyan-400">
        </div>
        <Contact />
        <div
            class="w-full h-1 bg-gradient-to-r dark:from-cyan-50 from-cyan-800 dark:to-cyan-50 to-cyan-800 via-cyan-300 dark:via-cyan-400">
        </div>
        <Projects />
    </div>
</template>