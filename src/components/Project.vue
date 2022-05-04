<template>
    <article
        class="gap-8 px-8 py-4 my-8 space-y-12 rounded-md shadow-md md:space-y-0 md:grid-cols-8 md:grid dark:shadow-cyan-400 shadow-cyan-800 ">

        <div class="order-1 col-start-5 col-end-11 row-start-1 space-y-8 md:text-right">
            <h3 class="mx-auto text-2xl text-cyan-800 dark:text-cyan-100">{{ data.title }}</h3>
            <p
                class="p-4 text-lg leading-7 tracking-wide text-cyan-100 dark:bg-cyan-100 shadow-lg shadow-cyan-900 dark:text-cyan-900 bg-cyan-900 rounded-md ">
                {{
                        data.desc
                }}</p>

            <h4 class="w-full mx-auto text-xl">Used <span class=" dark:text-cyan-200">tech</span>nologies :
            </h4>
            <ul class="flex w-full flex-wrap mx-auto md:justify-end gap-x-4">
                <li class="underline underline-offset-2 decoration-cyan-800 dark:decoration-cyan-300"
                    v-for="(item, index) in data.techs">
                    {{ item }}
                </li>
            </ul>
        </div>
        <div
            class="max-w-2xl col-start-1 col-end-6 row-start-1 px-4 pt-4 mx-auto border-t border-l md:pt-0 rounded-3xl dark:border-cyan-300 border-cyan-900">
            <img class="object-contain object-center w-full py-4 " v-bind:src="data.imgSrc" alt="project image">
            <div class="flex items-center justify-around max-w-xl py-2 mx-auto ">
                <a class="block cursor-pointer text-cyan-800 dark:text-cyan-200" href="#" target="_blank">
                    <span class="">
                        <svg class="w-8 h-8  transition-transform duration-75 transform cursor-pointer fill-cyan-800 stroke-cyan-800 dark:fill-cyan-200 dark:stroke-cyan-200  hover:scale-105 "
                            xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" stroke="currentColor"
                            stroke-width="2">
                            <path stroke-linecap="round" stroke-linejoin="round"
                                d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4" />
                        </svg>
                    </span>
                    <span class="text-center"> Code </span>
                </a>
                <a class="block cursor-pointer text-cyan-800 dark:text-cyan-200" :href="data.demoLink" target="_blank">


                    <i
                        class="w-8 h-8 block  transition-transform duration-75 transform cursor-pointer fill-cyan-800 stroke-cyan-800 dark:fill-cyan-200 dark:stroke-cyan-200  hover:scale-105 fa-solid fa-desktop"></i>

                    <span class="text-center"> Live </span>
                </a>
            </div>
        </div>

    </article>
</template>
<script>
export default {
    props: {
        // name: {
        //     type: String,
        //     default: 'John'
        // },
        // title: {
        //     type: String,
        //     default: 'John'
        // },
        data: {
            type: Object,
            default: function () {
                return {
                    title: { type: String },
                    desc: { type: String },
                    imgSrc: { type: String },
                    githubLink: { type: String },
                    demoLink: { type: String },
                    techs: { type: Array },
                }
            }
        }
    }
}
</script>