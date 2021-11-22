<template>
  <div>stage C</div>
</template>

<script>
export default {
  name: 'KeepAliveStageC',
  mounted(){
    console.log("mounted C")
  },
  destroyed(){
    console.log("destroyed C")
  }
};
</script>

<style lang="scss">
</style>
