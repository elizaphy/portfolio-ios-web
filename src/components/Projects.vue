<!-- src/components/Projects.vue -->
<template>
  <section class="py-20 bg-slate-50" id="Projects">
    <div class="container mx-auto px-6">
      <h2 class="text-4xl md:text-5xl font-light text-slate-900 mb-16 text-center">
        Featured Projects
      </h2>

      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8 max-w-6xl mx-auto">
        <div
          v-for="(project, index) in projects"
          :key="project.name"
          class="bg-white rounded-2xl overflow-hidden shadow-lg hover:shadow-2xl transition-all duration-500 hover:-translate-y-2 group"
          :style="{ animationDelay: `${index * 200}ms` }"
        >
          <div class="relative overflow-hidden">
            <img
              :src="project.image"
              :alt="project.name"
              class="w-full h-48 object-cover group-hover:scale-110 transition-transform duration-500"
            />
            <div class="absolute inset-0 bg-gradient-to-t from-black/20 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
          </div>

          <div class="p-6">
            <h3 class="text-xl font-semibold text-slate-900 mb-3">
              {{ project.name }}
            </h3>
            <p class="text-slate-600 mb-4 leading-relaxed">
              {{ project.description }}
            </p>

            <div class="flex flex-wrap gap-2 mb-6">
              <span
                v-for="tech in project.stack"
                :key="tech"
                class="px-3 py-1 bg-blue-50 text-blue-700 rounded-full text-sm font-medium"
              >
                {{ tech }}
              </span>
            </div>

            <div class="flex gap-3">
              <Button
                size="sm"
                class="bg-blue-600 hover:bg-blue-700 text-white rounded-full"
              >
                <ExternalLink class="w-4 h-4 mr-2" />
                App Store
              </Button>
              <Button
                variant="outline"
                size="sm"
                class="border-slate-300 text-slate-700 hover:bg-slate-50 rounded-full"
              >
                <Github class="w-4 h-4 mr-2" />
                GitHub
              </Button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ExternalLink, Github } from "lucide-vue-next";
import Button from "./ui/Button.vue";

const projects = [
  {
    name: "Mobile Banking",
    description:
      "A comprehensive banking app that allows users to check accounts, make payments, transfers and perform various banking tasks.",
    stack: ["Swift", "SwiftUI", "Security", "Core Data"],
    image:
      "https://images.unsplash.com/photo-1563013544-824ae1b704d3?w=600&h=400&fit=crop",
    appStore: "#",
    github: "#",
  },
  {
    name: "Speedy Gas",
    description:
      "An eCommerce platform focused on gas delivery services with real-time tracking and payment integration.",
    stack: ["Swift", "Objective-C", "REST API", "Maps"],
    image:
      "https://images.unsplash.com/photo-1578662996442-48f60103fc96?w=600&h=400&fit=crop",
    appStore: "#",
    github: "#",
  },
  {
    name: "Pukmak",
    description:
      "Advanced messaging and video calling application with end-to-end encryption and group chat features.",
    stack: ["Swift", "WebRTC", "Socket.IO", "Core Data"],
    image:
      "https://images.unsplash.com/photo-1577563908411-5077b6dc7624?w=600&h=400&fit=crop",
    appStore: "#",
    github: "#",
  },
  {
    name: "Kazoo",
    description:
      "Location-based app with GPS tracking, location history, group chat and SOS emergency features.",
    stack: ["Swift", "Core Location", "Real-time", "Maps"],
    image:
      "https://images.unsplash.com/photo-1551288049-bebda4e38f71?w=600&h=400&fit=crop",
    appStore: "#",
    github: "#",
  },
  {
    name: "Tesjor",
    description:
      "Food delivery platform connecting customers with restaurants, featuring real-time order tracking.",
    stack: ["Swift", "REST API", "Payment", "Notifications"],
    image:
      "https://images.unsplash.com/photo-1565299624946-b28f40a0ca4b?w=600&h=400&fit=crop",
    appStore: "#",
    github: "#",
  },
  {
    name: "MedVoice",
    description:
      "Health technology app using science-based technology for health condition detection and doctor consultation.",
    stack: ["Swift", "AI/ML", "Core ML", "HealthKit"],
    image:
      "https://images.unsplash.com/photo-1559757148-5c350d0d3c56?w=600&h=400&fit=crop",
    appStore: "#",
    github: "#",
  },
];
</script>
