<template>
  <div>
    <input type="text" :value="text" @input="$emit('change', $event.target.value)">
  </div>
</template>

<script>
export default {
  name: 'customModel',
  model: {
    prop: 'text',
    event:'change'
  },
  props:{
    text:String,
    default(){
      return ''
    }
  }
};
</script>

<style lang="scss">
</style>
