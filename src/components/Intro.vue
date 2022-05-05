<template>
    <section id="intro" class="max-w-6xl px-4 py-12 mx-auto dark:text-cyan-50 text-cyan-800">
        <p class="py-4 font-mono text-2xl leading-normal ">Hi, my name is
            <span class="block">
                <span
                    class=" text-4xl dark:text-cyan-200 leading-loose animate-underline w-fit text-cyan-900">Dhaifallah
                </span>
                <span
                    class=" text-4xl dark:text-cyan-200 leading-loose animate-underline w-fit text-cyan-900">Ahmed.</span>
            </span>
        </p>
        <p class="py-2 text-3xl leading-7">I'm a <span class="dark:text-cyan-200 text-cyan-900"> software engineer
                .</span></p>
        <p class="py-2 text-xl leading-7">I'm a <i class="font-semibold tracking-wide dark:text-cyan-200 text-cyan-900">
                Front-end
                Developer</i>, I work
            with
            HTML,CSS,Tailwind
            css,Javascript and React Js</p>
        <p class="py-2 text-xl leading-7">Currently I'm working on some Javascript and React Js
            <span class="tracking-wide hover:text-cyan-600 dark:text-cyan-200 text-cyan-900">
                <a href="#"> projects</a>
            </span>
            to Improve my skills
        </p>
        <SkillSet />
    </section>
</template>
<script>
import SkillSet from './SkillSet.vue'

export default {
    name: 'App',
    components: {
        SkillSet
    }
}
</script>