<script setup>
import { ref, onMounted, onBeforeUnmount, computed } from 'vue'

const props = defineProps({
    limit: { type: Number, required: false },
    searchTerm: { type: String, required: false, default: '' },
    showViewAll: { type: Boolean, required: false, default: true },
    showHeader: { type: Boolean, required: false, default: true }
})

const projects = ref([
    {
        id: 1,
        title: 'Luxury Fashion Brand',
        categories: ['Design', 'Development'],
        description: 'High-end fashion eCommerce experience with bespoke UI and micro-interactions.',
        image: 'https://images.unsplash.com/photo-1551650975-87deedd944c3?auto=format&fit=crop&w=1200&q=80',
        tech: ['Vue', 'Tailwind', 'GSAP']
    },
    {
        id: 2,
        title: 'Tech Startup Dashboard',
        categories: ['Design', 'Development'],
        description: 'Real-time analytics dashboard with modular widgets and dark mode.',
        image: 'https://images.unsplash.com/photo-1467232004584-a241de8bcf5d?auto=format&fit=crop&w=1200&q=80',
        tech: ['Vue', 'ECharts', 'Tailwind']
    },
    {
        id: 3,
        title: 'Corporate Website',
        categories: ['Design', 'Branding'],
        description: 'Polished corporate presence with brand system and editorial layouts.',
        image: 'https://images.unsplash.com/photo-1551434678-e076c223a692?auto=format&fit=crop&w=1200&q=80',
        tech: ['Nuxt', 'Tailwind']
    },
    {
        id: 4,
        title: 'Mobile App Design',
        categories: ['Design', 'Prototyping'],
        description: 'Mobile product design with interactive prototype and usability testing.',
        image: 'https://images.unsplash.com/photo-1522542550221-31fd19575a2d?auto=format&fit=crop&w=1200&q=80',
        tech: ['Figma', 'Framer']
    },
    {
        id: 5,
        title: 'Blog Platform',
        categories: ['Development'],
        description: 'Content platform with MDX support, search, and custom theme.',
        image: 'https://images.unsplash.com/photo-1486312338219-ce68d2c6f44d?auto=format&fit=crop&w=1200&q=80',
        tech: ['Vue', 'Content API']
    },
    {
        id: 6,
        title: 'E-commerce Solution',
        categories: ['Development'],
        description: 'Headless commerce storefront focused on performance and accessibility.',
        image: 'https://images.unsplash.com/photo-1522071820081-009f0129c71c?auto=format&fit=crop&w=1200&q=80',
        tech: ['Vue', 'Stripe', 'Tailwind']
    }
])

const activeCategory = ref('All')
const isModalOpen = ref(false)
const selectedProject = ref(null)

const categories = ref(['All', 'Design', 'Development', 'Branding', 'Prototyping'])

const filteredProjects = computed(() => {
    const byCategory = activeCategory.value === 'All'
        ? projects.value
        : projects.value.filter(p => p.categories.includes(activeCategory.value))
    const term = props.searchTerm?.toLowerCase().trim() || ''
    if (!term) return byCategory
    return byCategory.filter(p =>
        p.title.toLowerCase().includes(term) ||
        p.description.toLowerCase().includes(term) ||
        p.categories.join(' ').toLowerCase().includes(term) ||
        (p.tech?.join(' ') || '').toLowerCase().includes(term)
    )
})

const visibleProjects = computed(() => {
    if (Number.isFinite(props.limit) && props.limit > 0) {
        return filteredProjects.value.slice(0, props.limit)
    }
    return filteredProjects.value
})

function openModal(project) {
    selectedProject.value = project
    isModalOpen.value = true
}

function closeModal() {
    isModalOpen.value = false
    selectedProject.value = null
}

function onKeydown(e) {
    if (e.key === 'Escape') closeModal()
}

onMounted(() => {
    window.addEventListener('keydown', onKeydown)
})

onBeforeUnmount(() => {
    window.removeEventListener('keydown', onKeydown)
})
</script>

<template>
    <section id="portfolio" class="py-20 bg-gray-800">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center mb-16" v-if="showHeader">
                    <h2 class="text-3xl md:text-4xl font-bold mb-4">
                        <span class="gradient-text">My Portfolio</span>
                    </h2>
                    <p class="text-gray-400 max-w-2xl mx-auto">
                        A curated selection of my finest work, showcasing quality, creativity, and attention to detail.
                    </p>
                    <div class="w-20 h-1 bg-gradient-to-r from-amber-400 to-purple-600 mx-auto mt-4"></div>
                </div>
                
                <div class="mb-8 flex justify-center">
                    <div class="inline-flex rounded-md shadow-sm" role="group">
                        <button v-for="cat in categories" :key="cat" type="button"
                                @click="activeCategory = cat"
                                class="px-4 py-2 text-sm font-medium bg-gray-700 text-gray-300 hover:bg-gray-600 first:rounded-l-lg last:rounded-r-lg"
                                :class="{ 'bg-amber-500 text-white': activeCategory === cat }">
                            {{ cat }}
                        </button>
                    </div>
                </div>
                
                <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
                    <div v-for="project in visibleProjects" :key="project.id"
                         class="project-card glass-effect rounded-xl overflow-hidden transition-all duration-300 cursor-pointer"
                         @click="openModal(project)">
                        <div class="relative group">
                            <img :src="project.image" 
                                 :alt="project.title" 
                                 class="w-full h-64 object-cover">
                            <div class="absolute inset-0 bg-gradient-to-t from-black to-transparent opacity-0 group-hover:opacity-80 transition-opacity duration-300 flex items-end p-6">
                                <div>
                                    <h3 class="text-white text-xl font-bold mb-2">{{ project.title }}</h3>
                                    <p class="text-gray-300">{{ project.categories.join(', ') }}</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="text-center mt-12" v-if="showViewAll">
                    <router-link to="/portfolio" class="inline-flex items-center px-6 py-3 border border-amber-400 text-amber-400 font-medium rounded-full hover:bg-amber-400 hover:bg-opacity-10 transition-all duration-300">
                        View All Projects
                        <i class="fas fa-arrow-right ml-2"></i>
                    </router-link>
                </div>
            </div>

            <!-- Modal -->
            <transition name="fade">
                <div v-if="isModalOpen" class="fixed inset-0 z-50 flex items-center justify-center">
                    <div class="absolute inset-0 bg-black bg-opacity-60 backdrop-blur-sm" @click="closeModal"></div>
                    <div class="relative z-10 max-w-3xl w-11/12 md:w-3/4 lg:w-1/2">
                        <div class="glass-effect rounded-2xl overflow-hidden shadow-2xl border border-white/10">
                            <div class="relative">
                                <img v-if="selectedProject" :src="selectedProject.image" :alt="selectedProject.title" class="w-full h-64 object-cover">
                                <button @click="closeModal" aria-label="Close"
                                        class="absolute top-3 right-3 h-9 w-9 flex items-center justify-center rounded-full bg-white/10 hover:bg-white/20 text-white">
                                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-5 h-5">
                                        <path fill-rule="evenodd" d="M5.47 5.47a.75.75 0 011.06 0L12 10.94l5.47-5.47a.75.75 0 111.06 1.06L13.06 12l5.47 5.47a.75.75 0 11-1.06 1.06L12 13.06l-5.47 5.47a.75.75 0 01-1.06-1.06L10.94 12 5.47 6.53a.75.75 0 010-1.06z" clip-rule="evenodd" />
                                    </svg>
                                </button>
                            </div>
                            <div class="p-6">
                                <h3 class="text-2xl font-bold mb-2" v-if="selectedProject">{{ selectedProject.title }}</h3>
                                <p class="text-gray-300 mb-4" v-if="selectedProject">{{ selectedProject.description }}</p>
                                <div class="flex flex-wrap gap-2 mb-6" v-if="selectedProject">
                                    <span v-for="t in selectedProject.tech" :key="t" class="px-3 py-1 rounded-full text-sm bg-white/10 border border-white/10">
                                        {{ t }}
                                    </span>
                                </div>
                                <div class="flex justify-end gap-3">
                                    <button @click="closeModal" class="px-4 py-2 rounded-lg bg-white/10 hover:bg-white/20 text-white">Close</button>
                                    <a href="#" class="px-4 py-2 rounded-lg bg-gradient-to-r from-amber-500 to-purple-600 text-white">View Project</a>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </transition>
    </section>
</template>

<style>
.fade-enter-active, .fade-leave-active { transition: opacity .2s ease; }
.fade-enter-from, .fade-leave-to { opacity: 0; }
</style>