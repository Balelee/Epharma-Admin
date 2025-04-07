<script setup lang="ts">
import {
    ChartBarIcon,
    CogIcon,
    DocumentTextIcon,
    HomeIcon,
    UsersIcon
} from '@heroicons/vue/24/outline';

const menuItems = [
  { name: 'Dashboard', icon: HomeIcon, active: true },
  { name: 'Users', icon: UsersIcon },
  { name: 'Analytics', icon: ChartBarIcon },
  { name: 'Reports', icon: DocumentTextIcon },
  { name: 'Settings', icon: CogIcon }
]
</script>

<template>
  <aside id="sidebar" class="fixed top-0 left-0 z-20 flex flex-col flex-shrink-0 w-64 h-full pt-16 font-normal duration-75 transition-transform bg-white border-r border-gray-200">
    <div class="h-full px-3 py-4 overflow-y-auto">
      <ul class="space-y-2">
        <li v-for="item in menuItems" :key="item.name">
          <a href="#" :class="['flex items-center p-2 text-gray-900 rounded-lg hover:bg-gray-100', { 'bg-gray-100': item.active }]">
            <component :is="item.icon" class="w-6 h-6 text-gray-500 transition duration-75" />
            <span class="ml-3">{{ item.name }}</span>
          </a>
        </li>
      </ul>
    </div>
  </aside>
</template>