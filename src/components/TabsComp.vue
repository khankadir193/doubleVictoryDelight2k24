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
    gap: 30vw;
    justify-content: center;
    display: flex;
    align-items: center;
    justify-content: center;
    height: 1.93333rem;
    border-radius: 2rem;
    text-align: center;
    background: #973930;
    border: .02667rem solid #ffeea8;
    width: 78%;
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
    /* background-color: orange; */
    color: yellow;
    background: url('../assets/images/leaderboard_select.png');
    background-size: 100% 100%;
    background-repeat: no-repeat;
    background-position: center;
    /* height: 3vh; */
}

.tab-content {
    margin-top: 20px;
}
</style>