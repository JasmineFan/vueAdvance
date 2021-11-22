<template>
  <div>
    <ul ref="ultest">
      <li v-for="(item, index) in list" :key="index">
        {{ item }}
      </li>
    </ul>
    <button @click="addItem">add new one</button>
  </div>
</template>

<script>
export default {
  name: "nextTick",
  data() {
    return {
      list: ["a", "b", "c"],
    };
  },
  methods: {
    addItem() {
      this.list.push(`${Date.now()}`);
      this.list.push(`${Date.now()}`);
      this.list.push(`${Date.now()}`);
      this.$nextTick(() => {
        const ulItem = this.$refs.ultest;
        console.log(ulItem.childNodes.length);
      });
    },
  },
};
</script>

<style lang="scss">
</style>
