<template>
        <LeaderBoardDesc v-if="showLeaderBoard" :title="leaderBoardTitle" :description = "leaderDescription" />
</template>

<script>
import LeaderBoardDesc from './LeaderBoardDesc.vue';
export default {
    name: 'DailyComp',
    components:{
        LeaderBoardDesc
    },
    data() {
        return {
            showLeaderBoard: true,
            leaderBoardTitle: "OverAll",
            leaderDescription: " The Top 1 Rebate Card users with most beans get extra rewards."
        }
    }
}

</script>

<style lang="less" scoped>

</style>