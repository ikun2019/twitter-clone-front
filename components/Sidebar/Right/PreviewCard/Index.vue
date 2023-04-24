<template>
  <div class="m-2 overflow-hidden border bg-gray-50 rounded-2xl dark:bg-dim-700 border-white-200 dark:border-gray-700">
    <h1 class="p-3 text-xl font-extrabold text-gray-900 border-b dark:text-white">
      {{ title }}
    </h1>
    <slot></slot>
    <div class="p-3 text-sm text-blue-400 cursor-pointer hover:bg-gray-100 dark:hover:bg-dim-300">
      Show more
    </div>
  </div>
</template>

<script>
// const twitterBorderColor = 'border-white-200 dark:border-gray-700';
export default {
  props: {
    title: {
      type: String,
      required: true
    }
  }
}
</script>
