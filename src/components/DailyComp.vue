<template>
    <div class="leaderboard-des">
        <p>The Top 1 Rebate Card user with most beans get extra rewards.</p>
    </div>
</template>

<script>
export default {
    name: 'DailyComp'
}

</script>

<style lang="less" scoped>
.leaderboard-des {

    width: 80%;
    margin: 0 auto 0;
    border-radius: .34667rem;
    text-align: center;
    height: 3vh;
    display: flex;
    align-items: center;
    padding: 0 0 0 .24rem;
    background: rgba(119, 27, 24, .4);
    position: relative;
    top: -2.5rem;
    p {
        font-size: 3vw;
        font-family: Roboto-Regular;
        font-weight: 400;
        color: #ffe073;
    }
}
</style>