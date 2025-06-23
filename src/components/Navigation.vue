<template>
  <nav
    :class="[
      'fixed top-0 w-full z-50 transition-all duration-300',
      isScrolled
        ? 'bg-white/90 backdrop-blur-md shadow-sm'
        : 'bg-transparent'
    ]"
  >
    <div class="container mx-auto px-6 py-4">
      <div class="flex justify-between items-center">
        <div class="text-xl font-medium text-slate-900">AT</div>

        <div class="hidden md:flex space-x-8">
          <a
            v-for="item in navItems"
            :key="item"
            :href="'#' + item.toLowerCase()"
            @click="scrollToSection(item)"
            class="text-slate-700 hover:text-blue-600 transition-colors duration-300 font-medium"
          >
            {{ item }}
          </a>
        </div>
      </div>
    </div>
  </nav>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

const isScrolled = ref(false);
const navItems = ['About', 'Projects', 'Skills', 'Contact'];

const scrollToSection = (id) => {
  const el = document.getElementById(id);
  if (el) {
    el.scrollIntoView({ behavior: 'smooth' });
  }
};

onMounted(() => {
  window.addEventListener('scroll', scrollToSection);
});

onUnmounted(() => {
  window.removeEventListener('scroll', scrollToSection);
});
</script>
