<template>
  <div
    class="lg:flex space-x-4 bg-indigo-200 px-5 py-6 mb-5 rounded-md text-purple-800"
  >
    <div class="w-full lg:w-2/4">
      <img :src="image" class="h-full w-full object-cover" />
    </div>
    <div class="lg:w-2/4">
      <h2 class="mt-5 lg:mt-0 text-xl md:text-2xl lg:text-3xl pt-2 font-bold">
        📦 {{ title }}
      </h2>

      <div class="flex items-center p-1 mt-3">
        <span class="text-lg mr-5">社团:</span>
        <profile-card
          :name="artist.name"
          :avatar="artist.avatar"
          w="w-11"
          h="h-11"
        />
      </div>

      <div class="flex flex-col lg:flex-row lg:items-center p-1 mt-2">
        <span class="mr-3">最后更新:</span>
        <span class="bg-indigo-500 p-2 text-white mr-3 rounded-md">{{
          updated
        }}</span>
      </div>

      <div class="flex flex-col lg:flex-row lg:items-center p-1 mt-2">
        <span class="mr-3 mb-2 lg:mb-0">进度管理:</span>
        <DBLink v-for="sheet in sheets" :key="sheet.name" :link="sheet" />
      </div>

      <div class="flex flex-wrap items-center space-y-2 lg:space-y-0 p-1 mt-2">
        <span class="mr-3">数据库:</span>
        <DBLink v-for="db in DBs" :key="db.name" :link="db" />
      </div>

      <div class="flex flex-wrap items-center p-1 mt-2">
        <span class="mr-3 mb-2 lg:mb-0">进度:</span>

        <progress-bar :progress="progress" />
      </div>

      <div class="flex flex-wrap items-center justify-center p-1 mt-2">
        <span class="w-full mr-3">内容：</span>
        <content-progress
          v-for="content in contents"
          :key="content.id"
          :content="content"
        />
      </div>

      <div class="flex flex-wrap items-center p-1 mt-2">
        <span class="w-full lg:w-auto mr-3 mb-2 lg:mb-0">参与/贡献:</span>
        <profile-card
          v-for="contributor in contributors"
          :key="contributor.name"
          :avatar="contributor.avatar"
          :name="contributor.name"
          w="w-8"
          h="h-8"
        />
      </div>

      <div class="flex items-center p-1 mt-2 space-x-2">
        <button
          disabled
          class="bg-purple-600 bg-opacity-40 py-2 px-4 text-white rounded-lg shadow-md focus:outline-none"
        >
          🔍 查看详细 (咕咕咕)
        </button>
      </div>
    </div>
  </div>
</template>

<script>
import ContentProgress from "./ContentProgress.vue";
import DBLink from "./DBLink.vue";
import ProfileCard from "./ProfileCard.vue";
import ProgressBar from "./ProgressBar.vue";

export default {
  components: { ProfileCard, ProgressBar, DBLink, ContentProgress },
  props: [
    "title",
    "image",
    "artist",
    "updated",
    "DBs",
    "sheets",
    "progress",
    "contents",
    "contributors",
  ],
};
</script>

<style>
</style>