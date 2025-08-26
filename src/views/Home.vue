<script setup>
import Hero from '../components/Hero.vue';
import About from '../components/About.vue';
import Services from '../components/Services.vue';
import Portofolio from '../components/Portofolio.vue';
import Testimonials from '../components/Testimonials.vue';
import Contact from '../components/Contact.vue';
</script>

<template>
    <body class="bg-gray-900 text-gray-100 font-sans overflow-x-hidden">
        
    <hero />
    <about />    
    <services />
    <portofolio :limit="6" />
    <testimonials />
    <contact />
    
    </body>
</template>
