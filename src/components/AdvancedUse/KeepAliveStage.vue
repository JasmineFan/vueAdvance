<template>
  <div>
    <button @click="changeState('A')">A</button>
    <button @click="changeState('B')">B</button>
    <button @click="changeState('C')">C</button>

    <keep-alive>
      <keep-alive-a v-if="state === 'A'"></keep-alive-a>
      <keep-alive-b v-if="state === 'B'"></keep-alive-b>
      <keep-alive-c v-if="state === 'C'"></keep-alive-c>
    </keep-alive>
  </div>
</template>

<script>
import KeepAliveA from "./KeepAliveStageA.vue";
import KeepAliveB from "./KeepAliveStageB.vue";
import KeepAliveC from "./KeepAliveStageC.vue";
export default {
  name: "KeepAliveStage",
  components: {
    KeepAliveA,
    KeepAliveB,
    KeepAliveC,
  },
  data() {
    return {
      state: "A",
    };
  },
  methods: {
    changeState(state) {
      this.state = state;
    },
  },
};
</script>

<style lang="scss">
</style>
