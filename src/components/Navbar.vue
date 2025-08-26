<template>
        <nav class="glass-effect fixed w-full z-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between h-20 items-center">
                <div class="flex-shrink-0 flex items-center">
                    <span class="text-xl font-bold gradient-text">ALIFY</span>
                </div>
                <div class="hidden md:block">
                    <div class="ml-10 flex items-baseline space-x-8">
                        <router-link to="/" class="px-3 py-2 rounded-md text-white text-sm font-medium hover:text-amber-400 transition-colors">Home</router-link>
                        <router-link to="/about" class="px-3 py-2 rounded-md text-white text-sm font-medium hover:text-amber-400 transition-colors">About</router-link>
                        <a href="#services" class="px-3 py-2 rounded-md text-white text-sm font-medium hover:text-amber-400 transition-colors">Services</a>
                        <router-link to="/portfolio" class="px-3 py-2 rounded-md text-white text-sm font-medium hover:text-amber-400 transition-colors">Portfolio</router-link>
                        <a href="#testimonials" class="px-3 py-2 rounded-md text-white text-sm font-medium hover:text-amber-400 transition-colors">Testimonials</a>
                        <a href="#contact" class="px-3 py-2 rounded-md text-white text-sm font-medium hover:text-amber-400 transition-colors">Contact</a>
                    </div>
                </div>
                <div class="md:hidden">
                    <button id="menu-toggle" class="text-gray-300 hover:text-white focus:outline-none">
                        <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
                        </svg>
                    </button>
                </div>
            </div>
        </div>
        <!-- Mobile menu -->
        <div id="mobile-menu" class="hidden md:hidden glass-effect">
            <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3">
                <router-link to="/" class="block px-3 py-2 rounded-md text-white text-base font-medium hover:text-amber-400 transition-colors">Home</router-link>
                <router-link to="/about" class="block px-3 py-2 rounded-md text-white text-base font-medium hover:text-amber-400 transition-colors">About</router-link>
                <router-link  to="#services" class="block px-3 py-2 rounded-md text-white text-base font-medium hover:text-amber-400 transition-colors">Services</router-link>
                <router-link  to="/portfolio" class="block px-3 py-2 rounded-md text-white text-base font-medium hover:text-amber-400 transition-colors">Portfolio</router-link>
                <router-link  to="#testimonials" class="block px-3 py-2 rounded-md text-white text-base font-medium hover:text-amber-400 transition-colors">Testimonials</router-link>
                <router-link  to="#contact" class="block px-3 py-2 rounded-md text-white text-base font-medium hover:text-amber-400 transition-colors">Contact</router-link>
            </div>
        </div>
    </nav>
</template>