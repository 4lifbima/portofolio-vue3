<template>
     <section id="home" class="min-h-screen flex items-center justify-center relative overflow-hidden hero-pattern">
            <div class="absolute top-0 left-0 w-full h-full opacity-20">
                <div class="absolute top-1/4 left-1/4 w-64 h-64 bg-purple-500 rounded-full filter blur-3xl opacity-40"></div>
                <div class="absolute bottom-1/4 right-1/4 w-64 h-64 bg-amber-500 rounded-full filter blur-3xl opacity-40"></div>
            </div>
            
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-20 md:py-0 z-10">
                <div class="grid md:grid-cols-2 gap-12 items-center">
                    <div class="text-center md:text-left">
                        <h1 class="text-4xl md:text-6xl font-bold mb-6">
                            <span class="gradient-text">Creating Digital</span><br>
                            <span class="text-white">Webdeveloper</span>
                        </h1>
                        <p class="text-lg text-gray-300 mb-8 max-w-lg">
                            I craft premium digital experiences with meticulous attention to detail and innovative solutions that elevate brands.
                        </p>
                        <div class="flex flex-col sm:flex-row gap-4 justify-center md:justify-start">
                            <a href="#portfolio" class="px-8 py-3 bg-gradient-to-r from-amber-500 to-pink-500 text-white font-medium rounded-full hover:shadow-lg transition-all duration-300 transform hover:scale-105">
                                View My Work
                            </a>
                            <a href="#contact" class="px-8 py-3 border border-amber-400 text-amber-400 font-medium rounded-full hover:bg-amber-400 hover:bg-opacity-10 transition-all duration-300">
                                Contact Me
                            </a>
                        </div>
                    </div>
                    <div class="hidden md:block relative">
                        <div class="floating">
                            <div class="relative w-96 h-96 mx-auto">
                                <div class="absolute inset-0 bg-gradient-to-br from-amber-400 to-purple-600 rounded-full blur-xl opacity-30"></div>
                                <div class="relative w-full h-full flex items-center justify-center">
                                    <img src="/alifbimapradana.png" 
                                         alt="Professional Portrait" 
                                         class="w-80 h-80 object-cover rounded-full border-4 border-white border-opacity-20 shadow-2xl">
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="absolute bottom-10 left-1/2 transform -translate-x-1/2 animate-bounce">
                <a href="#about" class="text-gray-400 hover:text-white">
                    <i class="fas fa-chevron-down text-2xl"></i>
                </a>
            </div>
        </section>
</template>