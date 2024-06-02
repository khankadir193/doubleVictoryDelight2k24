<template>
        <LeaderBoardDesc v-if="showLeaderBoard" :title="leaderBoardTitle" :description = "leaderDescription" />
        <div class="trophy-container">
            <img src="../assets/images/picture_trophy.png" alt="trophy">
            <p>Come & join the event the first place waiting for you</p>
        </div>
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
.trophy-container{
    display: flex;
    margin: 3rem auto;
    justify-content: center;
    width: 25%;
    flex-direction: column;

    img{
        width: 100%;
    }

    p{
        width: 190%;
        color: white;
    }
}
</style>