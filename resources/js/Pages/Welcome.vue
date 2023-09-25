<script setup>
import { Head, Link } from "@inertiajs/vue3";
import FrontendLayout from "@/Layouts/Frontend.vue";
import Hero from "@/Components/Frontend/Hero.vue";
import About from "@/Components/Frontend/About.vue";
</script>

<template>
    <Head title="Welcome to Portfolio." />
    <FrontendLayout>
        <!-- Hero primary -->
        <Hero />
        <!-- Promote tail-100 -->
        <!-- About secondary -->
        <About />
        <!-- Skills tail-100 -->
        <!-- Portfolio primary -->
        <!-- Services secondary -->
        <!-- Contact primary -->
    </FrontendLayout>
</template>
