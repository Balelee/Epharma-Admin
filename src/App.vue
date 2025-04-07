<script setup lang="ts">
import NavBar from './components/Layouts/NavBar.vue';
import SideBar from './components/Layouts/SideBar.vue';


</script>

<template>
  <div class="min-h-screen bg-gray-50">
    <NavBar />
    <SideBar />
    <div class="p-4 lg:ml-64 pt-20">
      <!-- Main Content Area -->
      <div class="p-4 bg-white rounded-lg shadow">
        <h2 class="text-2xl font-bold mb-4">Welcome to Admin Dashboard</h2>
        <p class="text-gray-600">This is your main content area. Add your dashboard components here.</p>
      </div>
    </div>
  </div>
</template>