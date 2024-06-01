<template>
    <div>
        <div class="tabs">
            <button :class="{ active: currentTab === 'DailyComp' }" @click="currentTab = 'DailyComp'">Daily</button>
            <button :class="{ active: currentTab === 'OverallComp' }"
                @click="currentTab = 'OverallComp'">Overall</button>
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
    gap: 5vw;
    justify-content: center;
    display: flex;
    align-items: center;
    justify-content: center;
    height: 2.93333rem;
    border-radius: 2rem;
    text-align: center;
    background: #973930;
    border: .02667rem solid #ffeea8;
    width: 90%;
    margin: 3rem auto;
}

button {
    padding: 10px 20px;
    cursor: pointer;
    background: none;
    outline: none;
    border: none;
}

button.active {
    background-color: orange;
    color: white;
    
}

.tab-content {
    margin-top: 20px;
}
</style>