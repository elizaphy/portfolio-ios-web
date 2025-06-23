<template>
  <section class="py-20 bg-slate-50" id="Contact">
    <div class="container mx-auto px-6">
      <h2 class="text-4xl md:text-5xl font-light text-slate-900 mb-16 text-center">
        Let's Connect
      </h2>

      <div class="max-w-4xl mx-auto flex gap-5 justify-center items-center text-center">
        <!-- Contact Info -->
        <div class="space-y-8 mx-auto">
          <div>
            <!-- <h3 class="text-2xl font-medium text-slate-900 mb-4">Get in Touch</h3> -->
            <p class="text-lg text-slate-600 leading-relaxed">
              I'm always interested in new opportunities and exciting projects.
              Whether you're looking to build innovative mobile applications or need
              an experienced iOS developer to join your team, let's talk!
            </p>
          </div>

          <div class="space-y-4 mx-auto">
            <a
              href="mailto:limkimheng@gmail.com"
              class="flex items-center space-x-4 text-slate-700 hover:text-blue-600 transition-colors duration-300"
            >
              <Mail class="w-6 h-6" />
              <span class="text-lg">limkimheng@gmail.com</span>
            </a>
            <a
              href="http://linkedin.com/in/limkimheng"
              class="flex items-center space-x-4 text-slate-700 hover:text-blue-600 transition-colors duration-300"
            >
              <Linkedin class="w-6 h-6" />
              <span class="text-lg">LinkedIn Profile</span>
            </a>
            <a
              href="#"
              class="flex items-center space-x-4 text-slate-700 hover:text-blue-600 transition-colors duration-300"
            >
              <Github class="w-6 h-6" />
              <span class="text-lg">GitHub Profile</span>
            </a>
            <div class="flex items-center space-x-4 text-slate-700">
              <span class="text-lg">📱 +855 1055481</span>
            </div>
            <div class="text-slate-600 text-sm">
              <p>#16 Street 428, Sangkat Boeung Trobek</p>
              <p>Khan Chamkarmorn, Phnom Penh, Cambodia</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import { Mail, Github, Linkedin } from 'lucide-vue-next'
import Input from './ui/Input.vue'
import Button from './ui/Button.vue'

const form = ref({
  name: '',
  email: '',
  message: ''
})

const handleSubmit = () => {
  console.log("Form Submitted:", form.value)
  // TODO: Add API integration here
}
</script>
