<template>
    <section id="portfolio" class="py-20 bg-gray-800">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center mb-16">
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
                        <button type="button" class="px-4 py-2 text-sm font-medium rounded-l-lg bg-amber-500 text-white">
                            All
                        </button>
                        <button type="button" class="px-4 py-2 text-sm font-medium bg-gray-700 text-gray-300 hover:bg-gray-600">
                            Design
                        </button>
                        <button type="button" class="px-4 py-2 text-sm font-medium bg-gray-700 text-gray-300 hover:bg-gray-600">
                            Development
                        </button>
                        <button type="button" class="px-4 py-2 text-sm font-medium rounded-r-lg bg-gray-700 text-gray-300 hover:bg-gray-600">
                            Branding
                        </button>
                    </div>
                </div>
                
                <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
                    <!-- Project 1 -->
                    <div class="project-card glass-effect rounded-xl overflow-hidden transition-all duration-300">
                        <div class="relative group">
                            <img src="https://images.unsplash.com/photo-1551650975-87deedd944c3?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1074&q=80" 
                                 alt="Project 1" 
                                 class="w-full h-64 object-cover">
                            <div class="absolute inset-0 bg-gradient-to-t from-black to-transparent opacity-0 group-hover:opacity-80 transition-opacity duration-300 flex items-end p-6">
                                <div>
                                    <h3 class="text-white text-xl font-bold mb-2">Luxury Fashion Brand</h3>
                                    <p class="text-gray-300">UI/UX Design, Web Development</p>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Project 2 -->
                    <div class="project-card glass-effect rounded-xl overflow-hidden transition-all duration-300">
                        <div class="relative group">
                            <img src="https://images.unsplash.com/photo-1467232004584-a241de8bcf5d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1169&q=80" 
                                 alt="Project 2" 
                                 class="w-full h-64 object-cover">
                            <div class="absolute inset-0 bg-gradient-to-t from-black to-transparent opacity-0 group-hover:opacity-80 transition-opacity duration-300 flex items-end p-6">
                                <div>
                                    <h3 class="text-white text-xl font-bold mb-2">Tech Startup Dashboard</h3>
                                    <p class="text-gray-300">UI/UX Design, Frontend Development</p>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Project 3 -->
                    <div class="project-card glass-effect rounded-xl overflow-hidden transition-all duration-300">
                        <div class="relative group">
                            <img src="https://images.unsplash.com/photo-1551434678-e076c223a692?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80" 
                                 alt="Project 3" 
                                 class="w-full h-64 object-cover">
                            <div class="absolute inset-0 bg-gradient-to-t from-black to-transparent opacity-0 group-hover:opacity-80 transition-opacity duration-300 flex items-end p-6">
                                <div>
                                    <h3 class="text-white text-xl font-bold mb-2">Corporate Website</h3>
                                    <p class="text-gray-300">Web Design, Branding</p>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Project 4 -->
                    <div class="project-card glass-effect rounded-xl overflow-hidden transition-all duration-300">
                        <div class="relative group">
                            <img src="https://images.unsplash.com/photo-1522542550221-31fd19575a2d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80" 
                                 alt="Project 4" 
                                 class="w-full h-64 object-cover">
                            <div class="absolute inset-0 bg-gradient-to-t from-black to-transparent opacity-0 group-hover:opacity-80 transition-opacity duration-300 flex items-end p-6">
                                <div>
                                    <h3 class="text-white text-xl font-bold mb-2">Mobile App Design</h3>
                                    <p class="text-gray-300">UI/UX Design, Prototyping</p>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Project 5 -->
                    <div class="project-card glass-effect rounded-xl overflow-hidden transition-all duration-300">
                        <div class="relative group">
                            <img src="https://images.unsplash.com/photo-1486312338219-ce68d2c6f44d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1172&q=80" 
                                 alt="Project 5" 
                                 class="w-full h-64 object-cover">
                            <div class="absolute inset-0 bg-gradient-to-t from-black to-transparent opacity-0 group-hover:opacity-80 transition-opacity duration-300 flex items-end p-6">
                                <div>
                                    <h3 class="text-white text-xl font-bold mb-2">Blog Platform</h3>
                                    <p class="text-gray-300">Web Development, CMS Integration</p>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Project 6 -->
                    <div class="project-card glass-effect rounded-xl overflow-hidden transition-all duration-300">
                        <div class="relative group">
                            <img src="https://images.unsplash.com/photo-1522071820081-009f0129c71c?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80" 
                                 alt="Project 6" 
                                 class="w-full h-64 object-cover">
                            <div class="absolute inset-0 bg-gradient-to-t from-black to-transparent opacity-0 group-hover:opacity-80 transition-opacity duration-300 flex items-end p-6">
                                <div>
                                    <h3 class="text-white text-xl font-bold mb-2">E-commerce Solution</h3>
                                    <p class="text-gray-300">Full Stack Development</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="text-center mt-12">
                    <a href="#" class="inline-flex items-center px-6 py-3 border border-amber-400 text-amber-400 font-medium rounded-full hover:bg-amber-400 hover:bg-opacity-10 transition-all duration-300">
                        View All Projects
                        <i class="fas fa-arrow-right ml-2"></i>
                    </a>
                </div>
            </div>
        </section>
</template>