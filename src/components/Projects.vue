<template>
    <section id="projects" class="w-full p-4 my-8 text-white ">
        <div class="max-w-6xl mx-auto ">
            <h2 class="text-3xl text-center md:text-left "> Projects I worked on </h2>
            <Project :data="{
                title: 'Anime News',
                desc: 'Simple anime app to explore, search and filter animes,and get the latest anime news using jikan api.',
                imgSrc: 'https://user-images.githubusercontent.com/77447520/159186205-fa01583e-58f2-4490-aa51-5478e5aa6aad.png',
                githubLink: 'https://github.com/DevDhaif/my-anime',
                demoLink: 'https://my-anime-seven.vercel.app/',
                techs: ['HTML', 'React Js', 'Tailwind css', 'Axios']
            }" />


        </div>
    </section>
</template>
<script>
import Project from './Project.vue'

export default {
    name: 'App',
    components: {
        Project
    }
}
</script>