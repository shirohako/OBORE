<template>
  <div class="flex items-center mr-5">
    <img :src="avatar" class="rounded-full mr-2" :class="[w, h]" />
    <span> {{ name }} </span>
  </div>
</template>

<script>
export default {
  props: {
    name: String,
    avatar: String,
    w: { type: String, default: "w-16" },
    h: { type: String, default: "h-16" },
  },
};
</script>

<style>
</style>