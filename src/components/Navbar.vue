<script setup>
import logo from '@/assets/img/logo.png'
import { RouterLink } from 'vue-router'
</script>

<template>
    <nav class="sticky top-0 left-0 right-0 bg-green-700 border-b  border-green-500 z-50">
        <div class="mx-auto max-w-7xl px-2 sm:px-6 lg:px-8 ">
            <div class="flex h-20 items-center justify-between">
                <div class="flex flex-1 items-center justify-center md:items-stretch md:justify-start">
                    <!-- Logo -->
                    <a class="flex flex-shrink-0 items-center mr-4" href="index.html">
                        <img class="h-10 w-auto" :src="logo" alt="Vue Jobs" />
                        <span class="hidden md:block text-white text-2xl font-bold ml-2">Vue Jobs</span>
                    </a>
                    <div class="md:ml-auto">
                        <div class="flex space-x-2">
                            <router-link to="/"
                                class="text-white hover:bg-green-900 hover:text-white rounded-md px-3 py-2"
                                :active-class="'bg-green-900 text-white'">Home</router-link>
                            <router-link to="/jobs"
                                class="text-white hover:bg-green-900 hover:text-white rounded-md px-3 py-2"
                                :active-class="'bg-green-900 text-white'">Jobs</router-link>
                            <router-link to="/jobs/add"
                                class="text-white hover:bg-green-900 hover:text-white rounded-md px-3 py-2"
                                :active-class="'bg-green-900 text-white'">Add
                                Job</router-link>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </nav>
</template>

<style scoped></style>