<template>
  <section class="py-20 bg-white" id="Skills">
    <div class="container mx-auto px-6">
      <h2 class="text-4xl md:text-5xl font-light text-slate-900 mb-16 text-center">
        Skills & Expertise
      </h2>

      <div class="max-w-4xl mx-auto">
        <div class="grid md:grid-cols-2 gap-8">
          <div
            v-for="(skill, index) in skills"
            :key="skill.name"
            class="group"
            :style="{ animationDelay: `${index * 100}ms` }"
          >
            <div class="flex justify-between items-center mb-3">
              <span class="text-lg font-medium text-slate-900">
                {{ skill.name }}
              </span>
              <span class="text-slate-600">{{ skill.level }}%</span>
            </div>

            <div class="w-full bg-slate-100 rounded-full h-2 overflow-hidden">
              <div
                class="h-full bg-gradient-to-r from-blue-500 to-blue-600 rounded-full transition-all duration-1000 ease-out group-hover:from-blue-600 group-hover:to-blue-700 slide-in"
                :style="{ width: `${skill.level}%` }"
              ></div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
const skills = [
  { name: "Swift", level: 95 },
  { name: "Objective-C", level: 90 },
  { name: "SwiftUI", level: 88 },
  { name: "Java", level: 85 },
  { name: "Corona SDK", level: 80 },
  { name: "Titanium SDK", level: 75 },
  { name: "GitHub & GitLab", level: 90 },
  { name: "Unity 3D", level: 70 }
];
</script>

<style scoped>
@keyframes slideIn {
  from {
    transform: translateX(-100%);
  }
  to {
    transform: translateX(0);
  }
}
.slide-in {
  animation: slideIn 1s ease-out forwards;
}
</style>
