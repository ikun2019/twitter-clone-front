<template>
  <div :class="{ 'dark': darkMode }">
    <div class="bg-white dark:bg-dim-900">
      <div class="min-h-full">
        <div class="grid grid-cols-12 mx-auto sm:px-6 lg:max-w-7xl lg:px-8 lg:gap-10">
          <!-- Left sidebar -->
          <div class="hidden md:block xs:col-span-1 xl:col-span-2">
            <div class="sticky top-0">
              <sidebar-left />
            </div>
          </div>
          <!-- Main content -->
          <main class="col-span-12 md:col-span-8 xl:col-span-6 bg-red-50">
            <main-section :title="'Home'" :loading="false">
              Content
            </main-section>
          </main>
          <!-- Right sidebar -->
          <div class="col-span-12 md:col-span-3 xl:col-span-4 bg-blue-500">
            <div class="sticky top-0">
              <sidebar-right />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const darkMode = false;
</script>
