<template>
    <section id="projects" class="w-full p-4 my-8 dark:text-white text-cyan-800 ">
        <div class="flex flex-col max-w-6xl mx-auto gap-y-8">
            <h2 class="text-3xl text-center md:text-left "> Projects I worked on </h2>

            <ul class=" transition-all duration-500  ">
                <li v-for="project in projects" class="transition-all duration-200  group relative">
                    <Project :data="project" />
                </li>
            </ul>


        </div>
    </section>
</template>
<script>
import Project from './Project.vue'
import { projectsInfo, skillsData, skillsDataSecond } from "../data/data";


export default {
    name: 'App',
    components: {
        Project
    },
    data() {
        return {
            svgs: skillsData,
            secondSvgs: skillsDataSecond,
            projects: projectsInfo
        };
    },
    components: { Project }
}
</script>