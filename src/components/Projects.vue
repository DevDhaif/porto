<template>
    <section id="projects" class="w-full py-4 my-8 text-white ">
        <div class="max-w-6xl mx-auto ">
            <h2 class="text-3xl text-center md:text-left "> Projects I worked on </h2>
            <h3 class="text-2xl ">Latest Projects</h3>
            <Project :data="{
                title: 'Anime News',
                desc: ' simple anime ',
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