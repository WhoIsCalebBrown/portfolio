<script setup>
import { Head, Link } from "@inertiajs/vue3";
import FrontendLayout from "@/Layouts/Frontend.vue";
import Hero from "@/Components/Frontend/Hero.vue";
import About from "@/Components/Frontend/About.vue";
import Skills from "@/Components/Frontend/Skills.vue";

defineProps({
    skills: Object,
});
</script>

<template>
    <Head title="Welcome to portfolio" />
    <FrontendLayout>
        <!-- Hero primary -->
        <Hero />
        <!-- Promote tail-100 -->
        <!-- Skills tail-100 -->
        <Skills :skills="skills" />
        <!-- About secondary -->
        <About />

        <!-- Portfolio primary -->
        <!-- Services secondary -->
        <!-- Contact primary -->
    </FrontendLayout>
</template>
