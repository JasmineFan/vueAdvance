<template>
  <div>
    <p>vue 高级特性</p>
    <hr />
    <p>{{ name }}</p>
    <!-- <input type="text" v-model="name"> -->
    <!-- <custom-model v-model="name" /> -->
    <!-- <next-tick /> -->
    <!-- <slot-demo :url="website.url">
      {{website.title}}
    </slot-demo> -->
    <!-- <scoped-slot-demo :url="website.url">
      <template v-slot="slotProps">
        {{slotProps.slotData.title}}
      </template>
    </scoped-slot-demo> -->
    <!-- <div v-for="(val,key) in newsData" :key="key">
      <component :is="val.type"/>
    </div> -->
    <keep-alive-stage/>

  </div>
</template>

<script>
import customModel from "./customModel.vue";
import nextTick from "./nextTick.vue";
import SlotDemo from './SlotDemo.vue'
// import ScopedSlotDemo from './ScopedSlotDemo.vue'
import KeepAliveStage from './KeepAliveStage.vue';



export default {
  name: "index",
  components: {
    customModel,
    nextTick,
    SlotDemo,
    KeepAliveStage,
    ScopedSlotDemo: ()=>{import('./ScopedSlotDemo.vue')},

    KeepAliveStage
  },
  data() {
    return {
      name: "fan",
      website:{
        url:"http://parent.com",
        title:"parent"
      },
      NextTickName:'nextTick',
      newsData:{
        1:{type:'cv-text-input'},
        2:{type:'cv-radiobutton'},
        3:{type:'cv-fileupload'}
      }
    };
  },
};
</script>

<style lang="scss">
</style>
