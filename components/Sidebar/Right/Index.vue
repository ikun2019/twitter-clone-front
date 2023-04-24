<template>
  <div class="flex flex-col">
    <!-- Preview Card : What's happening -->
    <sidebar-right-preview-card :title="'What is happening'">
      <sidebar-right-preview-card-item v-for="(whatsHappening, index) in whatsHappeningItems" :key="index">
        <div>
          <h2 class="font-bold text-gray-800 text-md dark:text-white">
            {{ whatsHappening.title }}
          </h2>
          <p class="text-xs text-gray-400">
            {{ whatsHappening.count }}
          </p>
        </div>
      </sidebar-right-preview-card-item>
    </sidebar-right-preview-card>

    <!-- Preview Card : Who to follow -->
    <sidebar-right-preview-card :title="'Who to follow'">
      <sidebar-right-preview-card-item v-for="(whoToFollow, index) in whoToFollowItems" :key="index">
        <div class="flex flex-row justify-between p2">
          <div class="flex flex-row">
            <img class="w-10 h-10 rounded-full" :src="whoToFollow.image" :alt="whoToFollow.name">
            <div class="flex flex-col ml-2">
              <h1 class="text-sm font-bold text-gray-900 dark:text-white">{{ whoToFollow.name }}</h1>
              <p class="text-xs text-gray-400">{{ whoToFollow.handle }}</p>
            </div>
          </div>
          <div class="flex h-full">
            <button
              class="px-4 py-2 font-bold text-xs text-white dark:text-black bg-black dark:bg-white rounded-full">Follow</button>
          </div>
        </div>
      </sidebar-right-preview-card-item>
    </sidebar-right-preview-card>
  </div>
</template>

<script>
export default {
  data() {
    return {
      whatsHappeningItems: [
        {
          title: 'spaceX',
          count: '18.8k Tweets'
        },
        {
          title: 'Coding',
          count: '18.8k Tweets'
        },
        {
          title: 'art for all',
          count: '18.8k Tweets'
        },
      ],
      whoToFollowItems: [
        {
          name: 'Joe',
          handle: '@joe',
          image: 'https://picsum.photos/200/200'
        },
        {
          name: 'Joe',
          handle: '@joe',
          image: 'https://picsum.photos/200/200'
        },
        {
          name: 'Joe',
          handle: '@joe',
          image: 'https://picsum.photos/200/200'
        },
      ]
    };
  },
}
</script>
