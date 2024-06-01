<template>
    <div>
        <div class="tabs">
            <button :class="{ active: currentTab === 'DailyComp' }" @click="currentTab = 'DailyComp'">Daily</button>
            <button :class="{ active: currentTab === 'OverallComp' }" @click="currentTab = 'OverallComp'">Overall</button>
        </div>
        <div class="tab-content">
            <component :is="currentTab"></component>
        </div>
    </div>
</template>

<script>
import DailyComp from './DailyComp.vue'
import OverallComp from './OverAllComp.vue'

export default {
    data() {
        return {
            currentTab: 'DailyComp'
        }
    },
    components: {
        DailyComp,
        OverallComp
    }
}
</script>

<style>
.tabs {
    display: flex;
    gap: 10px;
    margin-top: 2rem;
    justify-content: center;
}

button {
    padding: 10px 20px;
    cursor: pointer;
}

button.active {
    background-color: orange;
    color: white;
}

.tab-content {
    margin-top: 20px;
}
</style>