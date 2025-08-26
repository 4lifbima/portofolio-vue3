<script setup>
import { ref, onMounted } from 'vue'
import Portofolio from '../components/Portofolio.vue'

const search = ref('')
const isLoading = ref(true)

onMounted(() => {
    setTimeout(() => {
        isLoading.value = false
    }, 2000)
})
</script>

<template>
    <body class="bg-gray-900 text-gray-100 font-sans overflow-x-hidden">
        <section class="pt-28 pb-6 bg-gradient-to-b from-gray-900 to-gray-800">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="flex flex-col md:flex-row md:items-end md:justify-between gap-4">
                    <div>
                        <h1 class="text-4xl md:text-5xl font-extrabold mb-2">
                            <span class="gradient-text">All Projects</span>
                        </h1>
                        <p class="text-gray-300">Browse the full archive of my work.</p>
                    </div>
                    <div class="w-full md:w-96">
                        <div class="relative">
                            <input v-model="search" type="text" placeholder="Search projects..." class="w-full glass-effect rounded-xl border border-white/10 px-4 py-3 pr-10 placeholder-gray-400 focus:outline-none" />
                            <span class="absolute right-3 top-1/2 -translate-y-1/2 text-gray-400">
                                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5">
                                  <path stroke-linecap="round" stroke-linejoin="round" d="M21 21l-3.5-3.5m1-5.5a7.5 7.5 0 11-15 0 7.5 7.5 0 0115 0z" />
                                </svg>
                            </span>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <div v-if="isLoading" class="py-10">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="mb-6 animate-pulse">
                    <div class="h-12 w-full md:w-96 bg-gray-700/60 rounded-xl"></div>
                </div>
                <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6 animate-pulse">
                    <div v-for="n in 6" :key="n" class="glass-effect rounded-xl overflow-hidden">
                        <div class="w-full h-64 bg-gray-700/60"></div>
                        <div class="p-6 space-y-3">
                            <div class="h-6 w-2/3 bg-gray-700/60 rounded"></div>
                            <div class="h-4 w-1/2 bg-gray-700/60 rounded"></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <Portofolio v-else :limit="0" :search-term="search" :show-view-all="false" :show-header="false" />
    </body>
</template>

