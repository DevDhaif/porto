<template>
    <article class="relative p-8 space-y-6 bg-[url('{{data.imgSrc}}')]  bg-blend-overlay">
        <h3 class="text-2xl">{{ data.title }}</h3>
        <h3 class="text-2xl">{{ data.imgSrc }}</h3>
        <p>{{ data.desc }}</p>
        <a href="#" target="_blank">Live</a>
        <a v-bind:href="data.demoLink" target="_blank">Demo</a>
        <h4 class="text-xl">Technologies used :</h4>
        <ul class="flex py-4 gap-x-4">
            <li v-for="(item, index) in data.techs">
                {{ item }}
            </li>
        </ul>

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