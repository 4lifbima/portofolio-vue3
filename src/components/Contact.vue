<template>
    <section id="contact" class="py-20 bg-gray-800">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center mb-16">
                    <h2 class="text-3xl md:text-4xl font-bold mb-4">
                        <span class="gradient-text">Get In Touch</span>
                    </h2>
                    <p class="text-gray-400 max-w-2xl mx-auto">
                        Have a project in mind or want to discuss potential collaboration? I'd love to hear from you.
                    </p>
                    <div class="w-20 h-1 bg-gradient-to-r from-amber-400 to-purple-600 mx-auto mt-4"></div>
                </div>
                
                <div class="grid md:grid-cols-2 gap-12">
                    <div>
                        <h3 class="text-2xl font-bold mb-6">Let's Talk About Your Project</h3>
                        <p class="text-gray-300 mb-8">
                            Whether you're looking to launch a new website, redesign an existing one, or develop a comprehensive digital strategy, I'm here to help. Fill out the form or contact me directly using the information below.
                        </p>
                        
                        <div class="space-y-4 mb-8">
                            <div class="flex items-start">
                                <div class="text-amber-400 mr-4 mt-1">
                                    <i class="fas fa-envelope text-xl"></i>
                                </div>
                                <div>
                                    <h4 class="font-bold text-white">Email</h4>
                                    <a href="mailto:contact@luxuryportfolio.com" class="text-gray-400 hover:text-amber-400 transition-colors">contact@luxuryportfolio.com</a>
                                </div>
                            </div>
                            
                            <div class="flex items-start">
                                <div class="text-amber-400 mr-4 mt-1">
                                    <i class="fas fa-phone-alt text-xl"></i>
                                </div>
                                <div>
                                    <h4 class="font-bold text-white">Phone</h4>
                                    <a href="tel:+1234567890" class="text-gray-400 hover:text-amber-400 transition-colors">+1 (234) 567-890</a>
                                </div>
                            </div>
                            
                            <div class="flex items-start">
                                <div class="text-amber-400 mr-4 mt-1">
                                    <i class="fas fa-map-marker-alt text-xl"></i>
                                </div>
                                <div>
                                    <h4 class="font-bold text-white">Location</h4>
                                    <p class="text-gray-400">New York, NY</p>
                                </div>
                            </div>
                        </div>
                        
                        <div class="flex space-x-4">
                            <a href="#" class="w-10 h-10 rounded-full bg-gray-700 flex items-center justify-center text-gray-300 hover:bg-amber-500 hover:text-white transition-colors">
                                <i class="fab fa-twitter"></i>
                            </a>
                            <a href="#" class="w-10 h-10 rounded-full bg-gray-700 flex items-center justify-center text-gray-300 hover:bg-amber-500 hover:text-white transition-colors">
                                <i class="fab fa-linkedin-in"></i>
                            </a>
                            <a href="#" class="w-10 h-10 rounded-full bg-gray-700 flex items-center justify-center text-gray-300 hover:bg-amber-500 hover:text-white transition-colors">
                                <i class="fab fa-dribbble"></i>
                            </a>
                            <a href="#" class="w-10 h-10 rounded-full bg-gray-700 flex items-center justify-center text-gray-300 hover:bg-amber-500 hover:text-white transition-colors">
                                <i class="fab fa-behance"></i>
                            </a>
                        </div>
                    </div>
                    
                    <div class="glass-effect p-8 rounded-xl">
                        <form>
                            <div class="grid grid-cols-1 gap-6">
                                <div>
                                    <label for="name" class="block text-sm font-medium text-gray-300 mb-1">Full Name</label>
                                    <input type="text" id="name" class="w-full px-4 py-3 bg-gray-700 border border-gray-600 rounded-lg focus:ring-2 focus:ring-amber-400 focus:border-transparent text-white placeholder-gray-400">
                                </div>
                                
                                <div>
                                    <label for="email" class="block text-sm font-medium text-gray-300 mb-1">Email Address</label>
                                    <input type="email" id="email" class="w-full px-4 py-3 bg-gray-700 border border-gray-600 rounded-lg focus:ring-2 focus:ring-amber-400 focus:border-transparent text-white placeholder-gray-400">
                                </div>
                                
                                <div>
                                    <label for="subject" class="block text-sm font-medium text-gray-300 mb-1">Subject</label>
                                    <input type="text" id="subject" class="w-full px-4 py-3 bg-gray-700 border border-gray-600 rounded-lg focus:ring-2 focus:ring-amber-400 focus:border-transparent text-white placeholder-gray-400">
                                </div>
                                
                                <div>
                                    <label for="message" class="block text-sm font-medium text-gray-300 mb-1">Message</label>
                                    <textarea id="message" rows="4" class="w-full px-4 py-3 bg-gray-700 border border-gray-600 rounded-lg focus:ring-2 focus:ring-amber-400 focus:border-transparent text-white placeholder-gray-400"></textarea>
                                </div>
                                
                                <div>
                                    <button type="submit" class="w-full px-6 py-3 bg-gradient-to-r from-amber-500 to-purple-600 text-white font-medium rounded-lg hover:shadow-lg transition-all duration-300 transform hover:scale-105">
                                        Send Message
                                    </button>
                                </div>
                            </div>
                        </form>
                    </div>
                </div>
            </div>
        </section>
</template>