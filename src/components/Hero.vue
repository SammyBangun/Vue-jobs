<script setup>
import programmingSample from '@/assets/doodles/programming.svg'
import processSample from '@/assets/doodles/thought-process.svg'

const props = defineProps({
    title: {
        type: String,
        required: true
    },
    subtitle: {
        type: String,
        required: true
    }
})
</script>

<template>
    <section class="relative overflow-hidden bg-gradient-to-r from-green-700 via-green-600 to-emerald-700 py-24 mb-8">
        <!-- Doodle Background -->
        <img :src="programmingSample" alt="Job Search Doodle"
            class="absolute bottom-0 left-0 w-64 opacity-20 pointer-events-none select-none animate-float" />

        <img :src="processSample" alt="Office Icon Doodle"
            class="absolute top-0 right-0 w-72 opacity-20 pointer-events-none select-none animate-float-slow" />

        <!-- Content -->
        <div class="max-w-7xl mx-auto px-6 sm:px-8 lg:px-12 flex flex-col items-center text-center relative z-10">
            <h1 class="text-4xl sm:text-5xl md:text-6xl font-extrabold text-white drop-shadow-lg tracking-tight">
                {{ title }}
            </h1>
            <p class="mt-4 text-lg sm:text-xl md:text-2xl text-green-100 max-w-2xl leading-relaxed">
                {{ subtitle }}
            </p>

            <!-- Decorative underline -->
            <div
                class="mt-6 h-1 w-32 bg-gradient-to-r from-lime-300 via-green-200 to-emerald-300 rounded-full shadow-md animate-pulse">
            </div>

            <!-- CTA Button (optional) -->
            <router-link to="/jobs"
                class="mt-10 inline-block bg-white text-green-700 font-semibold px-8 py-3 rounded-full shadow-lg hover:scale-105 hover:shadow-green-400/50 transition-transform duration-300">
                Explore Jobs
            </router-link>
        </div>
    </section>
</template>

<style scoped>
@keyframes float {
    0% {
        transform: translateY(0px);
    }

    50% {
        transform: translateY(-10px);
    }

    100% {
        transform: translateY(0px);
    }
}

.animate-float {
    animation: float 6s ease-in-out infinite;
}

.animate-float-slow {
    animation: float 10s ease-in-out infinite;
}
</style>
