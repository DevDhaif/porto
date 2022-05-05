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
  <div :class="isDark ? 'dark' : ''">
    <Transition appear @beforeEnter="beforeEnter" @enter="enter">
      <div
        class="fixed right-0 top-20 w-12 h-12 dark:text-cyan-800 text-cyan-100 dark:bg-cyan-100 bg-cyan-800  shadow-md shadow-cyan-800 rounded-full">
        <p id="num" class="text-center mt-2  ">0%</p>
      </div>
    </Transition>
    <!--
    <div class="fixed w-full z-20 ">
      <div
        class="relative dark:bg-cyan-100 bg-cyan-900 rounded-full text-right w-10  h-10 text-white shadow-xl shadow-red-500"
        id="scrolling">
        <span class="mt-4 " id="num">0 %</span>
      </div>
      <div id="scroll" class="dark:bg-cyan-100 bg-cyan-900 text-right w-0  h-2 text-white shadow-xl shadow-red-500">
      </div>
    </div>
    -->
    <TestNav isDark=false />
    <div
      class="w-full h-1 bg-gradient-to-r dark:from-cyan-50 from-cyan-800 dark:to-cyan-50 to-cyan-800 via-cyan-300 dark:via-cyan-400">
    </div>
    <Intro />
    <div
      class="w-full h-1 bg-gradient-to-r dark:from-cyan-50 from-cyan-800 dark:to-cyan-50 to-cyan-800 via-cyan-300 dark:via-cyan-400">
    </div>
    <Contact />
    <div
      class="w-full h-1 bg-gradient-to-r dark:from-cyan-50 from-cyan-800 dark:to-cyan-50 to-cyan-800 via-cyan-300 dark:via-cyan-400">
    </div>
    <Projects />
    <div
      class="w-full h-1 bg-gradient-to-r dark:from-cyan-50 from-cyan-800 dark:to-cyan-50 to-cyan-800 via-cyan-300 dark:via-cyan-400">
    </div>

    <Footer />
  </div>
</template>
<script>
import gsap from "gsap";

export default {

  name: 'App',
  data() {

    return {
      isDark: false,
    }
  },
  created() {
    window.addEventListener('scroll', this.handleScroll);
  },
  destroyed() {
    window.removeEventListener('scroll', this.handleScroll);
  },
  methods: {
    handleScroll(event) {
      document.addEventListener('scroll', function () {
        // This grabs the percentage the page is scrolled
        var h = document.documentElement,
          b = document.body,
          st = 'scrollTop',
          sh = 'scrollHeight';
        var scrollingBar = document.getElementById('scrolling');
        var percent = (h[st] || b[st]) / ((h[sh] || b[sh]) - h.clientHeight) * 100;
        // scrolling.style.width = percent + '%';
        document.getElementById('num').innerText = `${Math.floor(percent)} %`
      });
    },
    beforeEnter(el) {
      el.style.opacity = 0
      el.style.transform = 'translateY(200px)'
    },
    enter(el) {
      gsap.to(el, {
        opacity: 1,
        y: 0,
        duration: 1,
        delay: 1
      })
    }
  }
}
</script>
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