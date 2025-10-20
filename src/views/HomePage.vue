<script setup>
import { ref } from 'vue'

const name = 'Gary Davidson'
const title = 'Attorney legal counsel'
const description = 'Are you looking for a Ux/UI Designer who works hard but stays humble?'

const navItems = ['Home', 'About', 'Experience', 'Work', 'Services']
const activeNav = ref('Home')
</script>

<template>
  <div class="pa-6 min-h-screen bg-[#04131b] text-white">
    <!-- ===== Top Navigation Bar ===== -->
    <header class="flex justify-between items-center px-8 md:px-16 py-6 border-b border-gray-800">
      <!-- Logo -->
      <h1 class="text-xl font-bold tracking-wide text-[#d8ff00]">
        Gary Davidson
      </h1>

      <!-- Navigation Links -->
      <!-- <nav class="hidden md:flex items-center gap-8 text-gray-300">
        <a
          v-for="item in navItems"
          :key="item"
          href="#"
          @click.prevent="activeNav = item"
          class="relative font-medium hover:text-[#d8ff00] transition"
        >
          {{ item }}
          <span
            v-if="activeNav === item"
            class="absolute bottom-[-6px] left-0 w-full h-[2px] bg-[#d8ff00]"
          ></span>
        </a>
      </nav> -->

      <!-- Contact Button -->
      <v-btn
      href="mailto:attorneygarydavidson@pinnacleconsulting.com"
        variant="plain"
        size="large"
        class="!text-[#d8ff00] font-semibold border border-[#d8ff00] hover:!bg-[#d8ff00] hover:!text-[#04131b]"
      >
        Hire Us
        <v-icon icon="mdi-arrow-right" class="ml-2" />
      </v-btn>
    </header>

    <!-- ===== Hero Section ===== -->
    <section
      class="relative text-white py-24 overflow-hidden"
      style="background: linear-gradient(160deg, #04131b 0%, #07202e 50%, #0a2d42 100%)"
    >
      <div
        class="max-w-full mx-auto px-8 grid md:grid-cols-[60%_40%] gap-12 items-center min-h-[70vh]"
      >
        <!-- Left Content -->
        <div>
          <!-- Tagline -->
          <span
            class="px-4 py-1.5 bg-[#d8ff00]/10 text-sm rounded-full border border-[#d8ff00]/40 mb-6 inline-block"
          >
            Trusted Legal Representation
          </span>

          <!-- Main Headline -->
          <h1 class="text-4xl md:text-5xl font-bold mb-6 leading-tight">
            Protecting Your <span class="text-[#d8ff00]">Rights</span> & Securing Your Future
          </h1>

          <!-- Subheading / Description -->
          <p class="text-gray-300 mb-8 max-w-prose text-lg">
            Gary Davidson is an experienced attorney providing expert legal counsel in civil,
            corporate, and criminal matters. With years of proven success, he delivers strategic
            advice and representation tailored to your needs.
          </p>

          <!-- Action Buttons -->
          <div class="flex flex-col sm:flex-row gap-6 mb-16">
            <v-btn
              href="mailto:attorneygarydavidson@pinnacleconsulting.com"
              size="x-large"
              class="!text-[#04131b] font-semibold !bg-[#d8ff00] hover:!bg-[#c8f400]"
            >
              Contact Us
              <v-icon icon="mdi-arrow-right" class="ml-2" />
            </v-btn>
          </div>
        </div>

        <!-- Right Animated Icon -->
        <div class="relative flex items-center justify-center">
          <!-- Pulsating Glow Rings -->
          <div
            class="absolute w-56 h-56 rounded-full bg-[#d8ff00]/20 blur-xl animate-pulse-slow"
          ></div>
          <div
            class="absolute w-80 h-80 rounded-full bg-[#d8ff00]/10 blur-2xl animate-pulse-slower"
          ></div>

          <img
            src="https://plus.unsplash.com/premium_photo-1661964256419-4b4f1322852d?ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&q=80&w=691"
            alt="Profile photo"
            class="rounded-lg w-64 md:w-80 object-cover"
          />
        </div>
      </div>
    </section>

    <!-- ===== Footer Section ===== -->
<footer class="bg-[#04131b] text-gray-300 border-t border-gray-800 mt-20">
  

  <!-- Bottom Line -->
  <div class="border-t border-gray-800 mt-2 py-2 text-center text-xs text-gray-500">
    © {{ new Date().getFullYear() }} Gary Davidson, Esq. All Rights Reserved.
  </div>
</footer>

  </div>
</template>

<style scoped>
@import 'https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css';
.v-btn {
  text-transform: none;
}
@keyframes pulse-slow {
  0%,
  100% {
    transform: scale(1);
    opacity: 0.6;
  }
  50% {
    transform: scale(1.1);
    opacity: 1;
  }
}
.animate-pulse-slow {
  animation: pulse-slow 3s infinite;
}

@keyframes pulse-slower {
  0%,
  100% {
    transform: scale(1);
    opacity: 0.4;
  }
  50% {
    transform: scale(1.15);
    opacity: 0.8;
  }
}
.animate-pulse-slower {
  animation: pulse-slower 5s infinite;
}

@keyframes bounce-slow {
  0%,
  100% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(-10px);
  }
}
.animate-bounce-slow {
  animation: bounce-slow 3s infinite;
}

@keyframes pulse-bright {
  0%,
  100% {
    opacity: 0.6;
  }
  50% {
    opacity: 1;
  }
}
.animate-pulse-bright {
  animation: pulse-bright 2s infinite;
}
</style>
