<template>
  <a
    :href="link.url"
    class="bg-indigo-500 p-2 text-white mr-3 rounded-md"
    target="_blank"
    >{{ link.name }}</a
  >
</template>

<script>
export default {
  props: ["link"],
};
</script>

<style>
</style>