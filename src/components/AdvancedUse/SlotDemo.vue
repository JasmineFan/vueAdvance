<template>
  <a :href="url">
    <slot>默认的</slot>
  </a>
</template>

<script>
export default {
  name: 'SlotDemo',
  props:['url'],

};
</script>

<style lang="scss">
</style>
