<template>
  <section class="py-20 bg-white" id="About">
    <div class="container mx-auto px-6">
      <div class="max-w-4xl mx-auto">
        <h2 class="text-4xl md:text-5xl font-light text-slate-900 mb-16 text-center">
          About Me
        </h2>

        <div class="grid md:grid-cols-2 gap-12 items-center">
          <div class="space-y-6">
            <p class="text-lg text-slate-600 leading-relaxed">
              With over 10 years of experience in mobile development, I specialize in creating
              innovative iOS applications and cross-platform solutions. Currently serving as iOS Lead
              at eCam Solution, building secure mobile banking and e-commerce applications.
            </p>
            <p class="text-lg text-slate-600 leading-relaxed">
              My expertise spans from native iOS development with Swift and Objective-C to
              cross-platform solutions using Titanium SDK and Corona. I have a proven track record
              of publishing successful applications on the App Store.
            </p>

            <div class="grid grid-cols-2 gap-4 mt-8">
              <div
                v-for="(skill, index) in skills"
                :key="skill"
                class="bg-slate-50 rounded-lg p-3 text-center text-slate-700 hover:bg-blue-50 hover:text-blue-700 transition-all duration-300"
                :style="{ animationDelay: `${index * 100}ms` }"
              >
                {{ skill }}
              </div>
            </div>
          </div>

          <div class="relative">
            <div class="w-80 h-80 mx-auto bg-gradient-to-br from-blue-100 to-slate-100 rounded-3xl overflow-hidden shadow-2xl">
              <img
                src="/src/assets/image.png"
                alt="Lim Kim Heng"
                class="w-full h-full object-cover"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const skills = [
  "Swift & Objective-C",
  "SwiftUI",
  "Mobile Banking",
  "Cross-Platform",
  "Unity 3D",
  "API Integration",
];
</script>
