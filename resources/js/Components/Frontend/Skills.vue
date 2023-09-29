<script setup>
defineProps({
    skills: Object,
});
</script>
<template>
    <section class="bg-dark-secondary py-2">
        <div class="container mx-auto">
            <div class="grid grid-cols-7 md:grid-flow-col">
                <div
                    class="flex items-center justify-center"
                    v-for="skill in skills.data"
                    :key="skill.id"
                >
                    <img :src="skill.image" :alt="skill.name" class="lg:h-20" />
                </div>
            </div>
        </div>
    </section>
</template>
