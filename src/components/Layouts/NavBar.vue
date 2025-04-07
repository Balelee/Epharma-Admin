<script setup lang="ts">
import { Bars3Icon, BellIcon, XMarkIcon } from '@heroicons/vue/24/outline'
import { ref } from 'vue'

const isSidebarOpen = ref(true)

const toggleSidebar = () => {
  isSidebarOpen.value = !isSidebarOpen.value
  const sidebar = document.querySelector('#sidebar')
  sidebar?.classList.toggle('-translate-x-full')
}
</script>

<template>
  <nav class="bg-white border-b border-gray-200 fixed z-30 w-full">
    <div class="px-3 py-3 lg:px-5 lg:pl-3">
      <div class="flex items-center justify-between">
        <div class="flex items-center justify-between">
          <span class="self-center text-xl font-semibold sm:text-2xl whitespace-nowrap">
            E-pharma
          </span>

          <button @click="toggleSidebar" class="mr-2 text-gray-600 hover:text-gray-900">
            <Bars3Icon v-if="isSidebarOpen" class="w-6 h-6" />
            <XMarkIcon v-else class="w-6 h-6" />
          </button>
        </div>
        <div class="flex items-center">
          <button class="p-2 rounded-lg hover:bg-gray-100">
            <BellIcon class="w-6 h-6 text-gray-500" />
          </button>
          <div class="flex items-center ml-3">
            <div class="h-8 w-8 rounded-full bg-gray-200"></div>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>