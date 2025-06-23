<template>
  <section class="min-h-screen flex items-center justify-center bg-gradient-to-br from-slate-50 to-white relative overflow-hidden">
    <!-- Background decoration -->
    <div class="absolute inset-0 bg-grid-slate-100 [mask-image:linear-gradient(0deg,white,rgba(255,255,255,0.6))] -z-10"></div>

    <div class="container mx-auto px-6 text-center relative z-10">
      <div class="animate-fade-in">
        <h1 class="text-5xl md:text-7xl font-light text-slate-900 mb-6 tracking-tight">
          Lim <span class="font-medium">Kim Heng</span>
        </h1>
        <h2 class="text-2xl md:text-3xl text-slate-600 mb-8 font-light">
          Senior iOS Developer
        </h2>
        <p class="text-xl md:text-2xl text-slate-500 mb-12 max-w-2xl mx-auto leading-relaxed">
          Crafting seamless experiences for iPhone & iPad
        </p>

        <div class="flex flex-col sm:flex-row gap-4 justify-center items-center">
          <Button
            size="lg"
            class="bg-blue-600 hover:bg-blue-700 text-white px-8 py-4 rounded-full transition-all duration-300 hover:scale-105 shadow-lg hover:shadow-xl flex items-center"
          >
            View Work
            <ArrowRight class="ml-2 h-5 w-5" />
          </Button>

          <Button
            variant="outline"
            size="lg"
            class="border-slate-300 text-slate-700 hover:bg-slate-50 px-8 py-4 rounded-full transition-all duration-300 hover:scale-105 flex items-center"
          >
            Download CV
            <Download class="ml-2 h-5 w-5" />
          </Button>
        </div>
      </div>
    </div>

    <!-- Floating elements -->
    <div class="absolute top-20 left-10 w-20 h-20 bg-blue-100 rounded-full opacity-60 animate-pulse"></div>
    <div class="absolute bottom-20 right-10 w-32 h-32 bg-slate-100 rounded-full opacity-40 animate-pulse delay-1000"></div>
  </section>
</template>

<script setup lang="ts">

import { ArrowRight, Download } from 'lucide-vue-next'
import Button from './ui/Button.vue';
</script>
