<template>
  <div class="bg-purple-200 bg-opacity-50 p-8 pb-6 mt-10 mx-3 rounded-md">
    <div class="md:flex items-center">
      <img
        src="https://ae01.alicdn.com/kf/Hfa1623ced42045fc8f1bb4430ff70d13C.png"
        class="w-32 h-32 rounded-full mx-auto md:-mx-0"
      />
      <h1 class="md:ml-5 text-4xl text-center md:text-left">Project OBORE</h1>
    </div>
    <div class="mt-6">
      <div class="bg-purple-300 bg-opacity-60 p-3 rounded-md">
        <p class="mt-3 mb-1 ml-2 text-2xl">📝 关于</p>
        <div class="p-2">
          <p class="mb-2">一个面向收藏者的无损音乐合集制作计划</p>
          <p class="mb-2">仅仅因为喜欢在做 并没有任何盈利</p>
          <p class="mb-2">
            OBORE=溺れる, 灵感来自 *Luna 的
            <a
              href="https://www.youtube.com/watch?v=rpEObcGvxP4"
              target="_blank"
              >8.32</a
            >
            的歌词
          </p>
          <p class="mb-2">
            Icon 生成于
            <a href="https://waifulabs.com/" target="_blank">Waifu Labs</a>,
            页面由 Vite & Vue 3 & Tailwindcss 创建
          </p>
        </div>
      </div>

      <div class="bg-purple-300 bg-opacity-60 mt-6 p-3 rounded-md">
        <p class="mt-3 ml-2 text-2xl">✏️ 贡献者</p>
        <div
          class="mt-5 flex flex-col space-y-3 lg:flex-row lg:space-y-0 lg:items-center pl-2 pb-2"
        >
          <profile-card
            v-for="contributor in contributors"
            :key="contributor.name"
            :avatar="contributor.avatar"
            :name="contributor.name"
          />
        </div>
      </div>
    </div>
  </div>
</template>


<script>
import ProfileCard from "./ProfileCard.vue";
export default {
  components: { ProfileCard },
  data() {
    return {
      contributors: [
        {
          avatar:
            "https://ae01.alicdn.com/kf/Hd0e601f28fbb44c88e3267308838183f3.jpg",
          name: "ame",
        },
        {
          avatar:
            "https://ae01.alicdn.com/kf/H7567cc51653b4d969d4fd16ff223978c5.jpg",
          name: "月影清风",
        },
      ],
    };
  },
};
</script>


