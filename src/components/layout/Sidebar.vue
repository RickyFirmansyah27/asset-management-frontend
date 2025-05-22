<template>
  <aside class="bg-primary-700 text-white w-64 h-screen shadow-md flex flex-col">
    <div class="flex items-center px-4 py-4 border-b border-primary-600">
      <router-link to="/" class="flex items-center space-x-2">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M20 7l-8-4-8 4m16 0l-8 4m8-4v10l-8 4m0-10L4 7m8 4v10" />
        </svg>
        <span class="font-bold text-xl">AssetManagement</span>
      </router-link>
    </div>
    <nav class="flex-1 px-4 py-4 space-y-2">
      <router-link 
        to="/" 
        class="block px-3 py-2 rounded-md text-sm font-medium hover:bg-primary-600 transition"
        :class="{ 'bg-primary-800': $route.path === '/' }"
      >
        Dashboard
      </router-link>
      <router-link 
        to="/assets" 
        class="block px-3 py-2 rounded-md text-sm font-medium hover:bg-primary-600 transition"
        :class="{ 'bg-primary-800': $route.path.includes('/assets') }"
      >
        Assets
      </router-link>
    </nav>
  </aside>
</template>

<script>
export default {
  name: 'Sidebar'
}
</script>
