<script setup>
import { ref, onMounted } from 'vue'
import About from '../components/AboutComponent.vue'

const isLoading = ref(true)

onMounted(() => {
    // Simulate data load; replace with real load hook if available
    setTimeout(() => {
        isLoading.value = false
    }, 700)
})
</script>

<template>
    <body class="bg-gray-900 text-gray-100 font-sans overflow-x-hidden">
        <section class="pt-28 pb-10 bg-gradient-to-b from-gray-900 to-gray-800">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
                <h1 class="text-4xl md:text-5xl font-extrabold mb-4">
                    <span class="gradient-text">About Me</span>
                </h1>
                <p class="text-gray-300 max-w-3xl mx-auto">
                    Learn more about my background, skills, and the values that guide my work.
                </p>
            </div>
        </section>
        <div v-if="isLoading" class="py-12">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="grid md:grid-cols-2 gap-12 items-center animate-pulse">
                    <div>
                        <div class="w-full h-72 bg-gray-700/60 rounded-xl"></div>
                        <div class="mt-4 w-32 h-10 bg-gray-700/60 rounded-lg"></div>
                    </div>
                    <div>
                        <div class="h-8 w-64 bg-gray-700/60 rounded mb-6"></div>
                        <div class="space-y-3 mb-8">
                            <div class="h-4 w-full bg-gray-700/60 rounded"></div>
                            <div class="h-4 w-11/12 bg-gray-700/60 rounded"></div>
                            <div class="h-4 w-10/12 bg-gray-700/60 rounded"></div>
                        </div>
                        <div class="grid grid-cols-2 gap-4 mb-8">
                            <div class="h-6 w-40 bg-gray-700/60 rounded"></div>
                            <div class="h-6 w-40 bg-gray-700/60 rounded"></div>
                            <div class="h-6 w-40 bg-gray-700/60 rounded"></div>
                            <div class="h-6 w-40 bg-gray-700/60 rounded"></div>
                        </div>
                        <div class="space-y-4">
                            <div class="h-2 w-full bg-gray-700/60 rounded"></div>
                            <div class="h-2 w-11/12 bg-gray-700/60 rounded"></div>
                            <div class="h-2 w-10/12 bg-gray-700/60 rounded"></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <about v-else />
    </body>
</template>
