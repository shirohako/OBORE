<template>
  <ve-progress
    color="#7579ff"
    thickness="5px"
    empty-thickness="0px"
    :empty-color-fill="emptyColorFill"
    :size="160"
    line-mode="in 6"
    :legend="content.progress"
    :hideLegend="false"
    legendClass="text-lg font-bold"
    animation="loop 700 1000"
    dash="4"
    :progress="calculatedProgress"
  >
    <template #legend>
      <span class="text-base font-normal">/{{ content.total }}</span>
    </template>
    <template #legend-caption>
      <p class="text-sm font-bold text-purple-600">{{ content.name }}</p>
    </template>
  </ve-progress>
</template>

<script>
const waveColor = "#237cef";

export default {
  props: ["content", "color"],
  computed: {
    calculatedProgress() {
      return (this.content.progress * 100) / this.content.total;
    },
  },
  data: () => ({
    emptyColorFill: {
      radial: true,
      colors: [
        {
          color: waveColor,
          offset: "0",
          opacity: "0",
        },
        {
          color: waveColor,
          offset: "79",
          opacity: "0",
        },
        {
          color: waveColor,
          offset: "80",
          opacity: "0.2",
        },
        {
          color: waveColor,
          offset: "90",
          opacity: "0.02",
        },
        {
          color: waveColor,
          offset: "100",
          opacity: "0.00",
        },
      ],
    },
  }),
};
</script>

<style>
</style>