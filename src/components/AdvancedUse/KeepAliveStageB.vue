<template>
  <div>stage B</div>
</template>

<script>
export default {
  name: 'KeepAliveStageB',
  mounted(){
    console.log("mounted B")
  },
  destroyed(){
    console.log("destroyed B")
  }
};
</script>

<style lang="scss">
</style>
