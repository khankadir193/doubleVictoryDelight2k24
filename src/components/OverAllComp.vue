<template>
    <LeaderBoardDesc v-if="showLeaderBoard" :title="leaderBoardTitle" :description="leaderDescription"/>
</template>

<script>
import LeaderBoardDesc from './LeaderBoardDesc.vue';

export default {
    name: 'OverAllComp',
    components: {
        LeaderBoardDesc
    },
    data() {
        return {
            showLeaderBoard: true,
            leaderBoardTitle: "OverAll",
            leaderDescription: " The Top 5 Rebate Card users with most beans get extra rewards."
        }
    }
}

</script>

<style scoped>
h1 {
    color: black;
}
</style>