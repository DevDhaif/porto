<template>
    <article
        class="gap-8 px-8 py-4 my-8 space-y-10 rounded-md shadow-lg md:space-y-0 md:grid-cols-8 place-items-stretch md:grid shadow-cyan-300/30">

        <div class="order-1 col-start-5 col-end-11 row-start-1 space-y-8 md:text-right">
            <h3 class="mx-auto text-2xl text-cyan-300">{{ data.title }}</h3>
            <p class="p-4 text-lg leading-7 tracking-wide bg-gray-900 rounded-md ">{{ data.desc }}</p>

            <h4 class="w-full mx-auto text-xl">Used <span class="text-cyan-300">tech</span>nologies :</h4>
            <ul class="flex w-full mx-auto md:justify-end gap-x-4">
                <li class="underline underline-offset-2 decoration-cyan-300" v-for="(item, index) in data.techs">
                    {{ item }}
                </li>
            </ul>
        </div>
        <div
            class="max-w-2xl col-start-1 col-end-6 row-start-1 px-4 pt-4 mx-auto border-t border-l md:pt-0 rounded-3xl border-cyan-300">
            <img class="object-contain object-center w-full py-4 " v-bind:src="data.imgSrc" alt="project image">
            <div class="flex items-center justify-around max-w-xl py-2 mx-auto ">
                <a class="block cursor-pointer text-cyan-500 hover:text-cyan-400" href="#" target="_blank">
                    <span class="">
                        <svg class="w-8 h-8 transition-transform duration-75 transform cursor-pointer hover:scale-105 "
                            xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" stroke="currentColor"
                            stroke-width="2">
                            <path stroke-linecap="round" stroke-linejoin="round"
                                d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4" />
                        </svg>
                    </span>
                    <span class="text-center"> Code </span>
                </a>
                <a class="block cursor-pointer text-cyan-500 hover:text-cyan-400" v-bind:href="data.demoLink"
                    target="_blank">
                    <span aria-hidden="true">

                        <svg class="w-8 h-8 transition-transform duration-75 transform cursor-pointer hover:scale-105 "
                            xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" stroke="currentColor"
                            stroke-width="2">
                            <path stroke-linecap="round" stroke-linejoin="round"
                                d="M21 12a9 9 0 01-9 9m9-9a9 9 0 00-9-9m9 9H3m9 9a9 9 0 01-9-9m9 9c1.657 0 3-4.03 3-9s-1.343-9-3-9m0 18c-1.657 0-3-4.03-3-9s1.343-9 3-9m-9 9a9 9 0 019-9" />
                        </svg>
                    </span>
                    <span> Live </span>
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