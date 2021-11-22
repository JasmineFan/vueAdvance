<template>
  <div>stage A</div>
</template>

<script>
export default {
  name: 'KeepAliveStageA',
  mounted(){
    console.log("mounted A")
  },
  destroyed(){
    console.log("destroyed A")
  }
};
</script>

<style lang="scss">
</style>
