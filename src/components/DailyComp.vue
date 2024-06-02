<template>
    <LeaderBoardDesc v-if="showLeaderBoard" :title="leaderBoardTitle" :description="leaderDescription" />
    <div class="trophy-container">
        <img src="../assets/images/picture_trophy.png" alt="trophy">
        <p>Come & join the event the first place waiting for you</p>
    </div>
    <div class="footer"> Have any questions? We'd love to hear from you. <br>
        Please contact us via WhatsApp. <br> Roman &amp; English:
        <span class="color_yellow">+1(442)228-3245</span>. Thank you!
        <div class="line"></div>
        <div class="footer_text">All rights reserved by Oyetalk</div>
    </div>
</template>

<script>
import LeaderBoardDesc from './LeaderBoardDesc.vue';
export default {
    name: 'DailyComp',
    components: {
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
.trophy-container {
    margin: 3rem auto;
    text-align: center;

    img {
        width: 20%;
    }

    p {
        width: 53%;
        color: white;
        margin: 0 auto;
        font-size: 4vw;
        text-shadow: 0 0 .08rem #0c1a75;
    }
}

.footer {
    margin-top: .53333rem;
    text-align: center;
    padding: 0 .56rem;
    font-size: 4vw;
    overflow: hidden;
    line-height: 1.4;
    color: #fff
}

.color_yellow {
    color: yellow;
}

.line {
    width: 65%;
    margin: .26667rem auto;
    height: .02667rem;
    background: #fff;
    opacity: .35;
}
</style>