<template>
  <nuxt-link to="#"
    class="flex items-center p-3 w-min hover:bg-gray-200 rounded-full text-black dark:hover:bg-dim-200 dark:text-white"
    :class="transition">
    <div class="w-6 h-6 text-dark">
      <slot name="icon"></slot>
    </div>
    <div class="ml-4 text-xl hidden xl:block">
      <slot name="name"></slot>
    </div>
  </nuxt-link>
</template>

<script>
const transition = 'transition ease-in-out duration-350';
export default {

}
</script>