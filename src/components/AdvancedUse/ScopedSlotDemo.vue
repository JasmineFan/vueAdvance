<template>
  <a :href="url">
    <slot :slotData="website">{{ website.title }}</slot>
  </a>
</template>

<script>
export default {
  name: "ScopedSlotDemo",
  props: ["url"],
  data() {
    return {
      website: {
        url: "http://child.com",
        title: "child"
      },
    };
  },
};
</script>

<style lang="scss">
</style>
