<template>
    <nav
        class="relative flex flex-col justify-between w-full max-w-6xl p-4 mx-auto font-mono text-white gap-y-4 md:flex-row">
        <div class="flex mx-0 mr-auto sm:mx-auto md:mx-0 gap-x-4">
            <h1 class="text-3xl text-center md:text-left"><a class="flex justify-center gap-4 " href="#index.html">
                    <svg class="w-8 fill-cyan-400 " xmlns="http://www.w3.org/2000/svg" viewBox="0 0 640 512">
                        <path
                            d="M414.8 40.79L286.8 488.8C281.9 505.8 264.2 515.6 247.2 510.8C230.2 505.9 220.4 488.2 225.2 471.2L353.2 23.21C358.1 6.216 375.8-3.624 392.8 1.232C409.8 6.087 419.6 23.8 414.8 40.79H414.8zM518.6 121.4L630.6 233.4C643.1 245.9 643.1 266.1 630.6 278.6L518.6 390.6C506.1 403.1 485.9 403.1 473.4 390.6C460.9 378.1 460.9 357.9 473.4 345.4L562.7 256L473.4 166.6C460.9 154.1 460.9 133.9 473.4 121.4C485.9 108.9 506.1 108.9 518.6 121.4V121.4zM166.6 166.6L77.25 256L166.6 345.4C179.1 357.9 179.1 378.1 166.6 390.6C154.1 403.1 133.9 403.1 121.4 390.6L9.372 278.6C-3.124 266.1-3.124 245.9 9.372 233.4L121.4 121.4C133.9 108.9 154.1 108.9 166.6 121.4C179.1 133.9 179.1 154.1 166.6 166.6V166.6z" />
                    </svg>
                    <span> Dhaif</span>
                </a>
            </h1>
        </div>
        <button @click="openMenu" class="absolute p-4 top-2 right-5 md:hidden">
            <span v-show="!open"><i class="text-white transition-all duration-500 ease-in fa-solid fa-bars"></i></span>
            <span v-show="open"><i class="text-white transition-all duration-500 ease-in fa-solid fa-xmark"></i></span>
        </button>
        <ul class="absolute flex flex-col flex-wrap items-start justify-between w-full px-4 duration-500 ease-in bg-gray-800 shadow-md bg-opacity-80 top-20 md:w-auto md:static gap-x-8 sm:flex-row shadow-cyan-300 md:shadow-none"
            :class="[open ? 'left-0' : '-left-[120%]']">
            <li class="my-4 animate-underline md:my-0" v-for="link in Links" :key="link.name">
                <a href={{link.link}} class="text-lg hover:text-cyan-300">{{ link.name }}</a>
            </li>
            <li class="my-4 md:my-0">
                <a class="block hover:text-cyan-400" href="https://github.com/DevDhaif" target="_blank">
                    <span class=" fill-cyan-200" aria-hidden="true">
                        <svg class="w-8 h-8 transition-transform duration-75 transform cursor-pointer hover:scale-105 "
                            xmlns="http://www.w3.org/2000/svg" viewBox="0 0 496 512">
                            <path
                                d="M165.9 397.4c0 2-2.3 3.6-5.2 3.6-3.3.3-5.6-1.3-5.6-3.6 0-2 2.3-3.6 5.2-3.6 3-.3 5.6 1.3 5.6 3.6zm-31.1-4.5c-.7 2 1.3 4.3 4.3 4.9 2.6 1 5.6 0 6.2-2s-1.3-4.3-4.3-5.2c-2.6-.7-5.5.3-6.2 2.3zm44.2-1.7c-2.9.7-4.9 2.6-4.6 4.9.3 2 2.9 3.3 5.9 2.6 2.9-.7 4.9-2.6 4.6-4.6-.3-1.9-3-3.2-5.9-2.9zM244.8 8C106.1 8 0 113.3 0 252c0 110.9 69.8 205.8 169.5 239.2 12.8 2.3 17.3-5.6 17.3-12.1 0-6.2-.3-40.4-.3-61.4 0 0-70 15-84.7-29.8 0 0-11.4-29.1-27.8-36.6 0 0-22.9-15.7 1.6-15.4 0 0 24.9 2 38.6 25.8 21.9 38.6 58.6 27.5 72.9 20.9 2.3-16 8.8-27.1 16-33.7-55.9-6.2-112.3-14.3-112.3-110.5 0-27.5 7.6-41.3 23.6-58.9-2.6-6.5-11.1-33.3 2.6-67.9 20.9-6.5 69 27 69 27 20-5.6 41.5-8.5 62.8-8.5s42.8 2.9 62.8 8.5c0 0 48.1-33.6 69-27 13.7 34.7 5.2 61.4 2.6 67.9 16 17.7 25.8 31.5 25.8 58.9 0 96.5-58.9 104.2-114.8 110.5 9.2 7.9 17 22.9 17 46.4 0 33.7-.3 75.4-.3 83.6 0 6.5 4.6 14.4 17.3 12.1C428.2 457.8 496 362.9 496 252 496 113.3 383.5 8 244.8 8zM97.2 352.9c-1.3 1-1 3.3.7 5.2 1.6 1.6 3.9 2.3 5.2 1 1.3-1 1-3.3-.7-5.2-1.6-1.6-3.9-2.3-5.2-1zm-10.8-8.1c-.7 1.3.3 2.9 2.3 3.9 1.6 1 3.6.7 4.3-.7.7-1.3-.3-2.9-2.3-3.9-2-.6-3.6-.3-4.3.7zm32.4 35.6c-1.6 1.3-1 4.3 1.3 6.2 2.3 2.3 5.2 2.6 6.5 1 1.3-1.3.7-4.3-1.3-6.2-2.2-2.3-5.2-2.6-6.5-1zm-11.4-14.7c-1.6 1-1.6 3.6 0 5.9 1.6 2.3 4.3 3.3 5.6 2.3 1.6-1.3 1.6-3.9 0-6.2-1.4-2.3-4-3.3-5.6-2z" />
                        </svg>
                    </span>
                    <span class="sr-only">Github</span>
                </a>
            </li>
            <li class="my-4 md:my-0">
                <a class="block hover:text-cyan-400" href="https://www.linkedin.com/in/dhaifallah-ahmed-160490203/">
                    <span class="fill-cyan-200" aria-hidden="true">
                        <svg class="w-8 h-8 transition-transform duration-75 transform cursor-pointer hover:scale-105"
                            xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512">
                            <path
                                d="M416 32H31.9C14.3 32 0 46.5 0 64.3v383.4C0 465.5 14.3 480 31.9 480H416c17.6 0 32-14.5 32-32.3V64.3c0-17.8-14.4-32.3-32-32.3zM135.4 416H69V202.2h66.5V416zm-33.2-243c-21.3 0-38.5-17.3-38.5-38.5S80.9 96 102.2 96c21.2 0 38.5 17.3 38.5 38.5 0 21.3-17.2 38.5-38.5 38.5zm282.1 243h-66.4V312c0-24.8-.5-56.7-34.5-56.7-34.6 0-39.9 27-39.9 54.9V416h-66.4V202.2h63.7v29.2h.9c8.9-16.8 30.6-34.5 62.9-34.5 67.2 0 79.7 44.3 79.7 101.9V416z" />
                        </svg>
                    </span>
                    <span class="sr-only">LinkedIn</span>
                </a>
            </li>
        </ul>
    </nav>
</template>
<script >
import { ref } from "vue"

export default {
    data() {
        return {
            Links: [
                { name: 'Projects', link: '#projects' },
                { name: 'About', link: '#about.html' },
                { name: 'Contact', link: '#contact' },
                { name: 'Resume', link: '../../public/ex.pdf' },

            ],
            open: ref(false),
            openMenu() {
                this.open = !this.open
                return this.open
            }
        }
    }
}
</script>