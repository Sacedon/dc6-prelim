<template>
    <nav class="space-y-4">
      <!-- Logo and Title -->
      <div class="text-center">
        <Link href="/dashboard" class="flex flex-col items-center space-x-2">
          <img
            src="@/Components/logo/logo.png"
            alt="Logo"
            class="w-16 h-16 rounded-full mb-2"
          />
          <span
            v-if="!isCollapsed"
            class="text-2xl text-white font-extrabold"
          >
            Admin
          </span>
        </Link>
      </div>

      <!-- Horizontal Line -->
      <hr class="mt-4">

      <!-- Navigation Label -->


      <!-- Link Section -->
      <LinkSection :isCollapsed="isCollapsed" />
    </nav>
  </template>

  <script setup>
  import LinkSection from '@/Components/LinkSection.vue';
  import { Link } from '@inertiajs/vue3';

  const props = defineProps({
    isCollapsed: Boolean,
  });
  </script>

  <style scoped>
  /* Add custom styles here if needed */
  </style>
