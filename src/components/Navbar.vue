<template>
        <nav class="glass-effect fixed w-full z-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between h-20 items-center">
                <div class="flex-shrink-0 flex items-center">
                    <span class="text-xl font-bold gradient-text">ALIFY</span>
                </div>
                <div class="hidden md:block">
                    <div class="ml-10 flex items-baseline space-x-8">
                        <a href="#home" class="px-3 py-2 rounded-md text-white text-sm font-medium hover:text-amber-400 transition-colors">Home</a>
                        <a href="#about" class="px-3 py-2 rounded-md text-white text-sm font-medium hover:text-amber-400 transition-colors">About</a>
                        <a href="#services" class="px-3 py-2 rounded-md text-white text-sm font-medium hover:text-amber-400 transition-colors">Services</a>
                        <a href="#portfolio" class="px-3 py-2 rounded-md text-white text-sm font-medium hover:text-amber-400 transition-colors">Portfolio</a>
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
                <a href="#home" class="block px-3 py-2 rounded-md text-white text-base font-medium hover:text-amber-400 transition-colors">Home</a>
                <a href="#about" class="block px-3 py-2 rounded-md text-white text-base font-medium hover:text-amber-400 transition-colors">About</a>
                <a href="#services" class="block px-3 py-2 rounded-md text-white text-base font-medium hover:text-amber-400 transition-colors">Services</a>
                <a href="#portfolio" class="block px-3 py-2 rounded-md text-white text-base font-medium hover:text-amber-400 transition-colors">Portfolio</a>
                <a href="#testimonials" class="block px-3 py-2 rounded-md text-white text-base font-medium hover:text-amber-400 transition-colors">Testimonials</a>
                <a href="#contact" class="block px-3 py-2 rounded-md text-white text-base font-medium hover:text-amber-400 transition-colors">Contact</a>
            </div>
        </div>
    </nav>
</template>