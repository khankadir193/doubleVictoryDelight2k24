<template>
    <div>
      <div class="tabs">
        <button @click="currentTab = 'DailyComp'">Tab 1</button>
        <button @click="currentTab = 'OverAllComp'">Tab 2</button>
      </div>
      <div class="tab-content">
        <component :is="currentTab"></component>
      </div>
    </div>
  </template>
  
  <script>
  import DailyComp from './DailyComp.vue';
  import OverAllComp from './OverAllComp.vue'
  
  export default {
    data() {
      return {
        currentTab: 'DailyComp'
      }
    },
    components: {
        DailyComp,
        OverAllComp
    }
  }
  </script>
  
  <style>
  .tabs {
    display: flex;
    justify-content: center;
    gap: 10px;
    margin: 3rem auto;
  }
  
  .tab-content {
    margin-top: 20px;
  }
  </style>
  