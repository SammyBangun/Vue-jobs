<script setup>
import logo from '@/assets/img/K2.jpg'
import { RouterLink } from 'vue-router'
</script>

<template>
    <nav
        class="sticky top-0 left-0 right-0 z-50 bg-gradient-to-r from-green-700 via-green-600 to-green-800 border-b border-green-500 shadow-lg backdrop-blur-md bg-opacity-90">
        <div class="mx-auto max-w-7xl px-2 sm:px-6 lg:px-8">
            <div class="flex h-20 items-center justify-between">
                <!-- Logo -->
                <div class="flex items-center space-x-3">
                    <router-link to="/" class="flex items-center space-x-2">
                        <img class="h-10 w-10 rounded-full border-2 border-green-200 shadow-md hover:scale-105 transition-transform duration-300"
                            :src="logo" alt="Vue Jobs" />
                        <span
                            class="hidden md:block text-white text-3xl font-extrabold tracking-wide hover:text-green-200 transition-colors">
                            Jobs
                        </span>
                    </router-link>
                </div>

                <!-- Link -->
                <div class="flex space-x-2 md:space-x-4">
                    <router-link to="/"
                        class="relative group text-white/90 px-4 py-2 font-semibold tracking-wide transition-all duration-300"
                        :active-class="'text-white'">
                        Home
                        <span
                            class="absolute left-0 bottom-0 w-0 h-[2px] bg-gradient-to-r from-green-400 via-green-300 to-green-500 transition-all duration-500 group-hover:w-full"></span>
                    </router-link>

                    <router-link to="/jobs"
                        class="relative group text-white/90 px-4 py-2 font-semibold tracking-wide transition-all duration-300"
                        :active-class="'text-white'">
                        Jobs
                        <span
                            class="absolute left-0 bottom-0 w-0 h-[2px] bg-gradient-to-r from-green-400 via-green-300 to-green-500 transition-all duration-500 group-hover:w-full"></span>
                    </router-link>

                    <router-link to="/jobs/add"
                        class="relative group text-white/90 px-4 py-2 font-semibold tracking-wide transition-all duration-300"
                        :active-class="'text-white'">
                        Add Job
                        <span
                            class="absolute left-0 bottom-0 w-0 h-[2px] bg-gradient-to-r from-green-400 via-green-300 to-green-500 transition-all duration-500 group-hover:w-full"></span>
                    </router-link>
                </div>
            </div>
        </div>
    </nav>
</template>

<style scoped>
nav {
    transition: background 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
}

.router-link-active {
    color: #fff !important;
    text-shadow: 0 0 10px rgba(72, 255, 133, 0.7);
}

.group:hover {
    transform: scale(1.05);
    text-shadow: 0 0 12px rgba(144, 238, 144, 0.8);
}
</style>
