<template>
    <div>
        <div class="leaderboard-des">
            <!-- <p>The Top 1 Rebate Card user with most beans get extra rewards.</p> -->
            <p>{{ description }}</p>
        </div>
        <div class="userColumn">
            <div>User</div>
            <div>Rebate beans</div>
            <div>Reward</div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'LeaderBoardDesc',
    props:{
        title:{
            type:String,
            required:true
        },
        description:{
            type:String,
            required:true,
            default:''
        }
    }
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
.userColumn{
    display: grid;
    grid-template-columns: 24% 52% 17%;
    text-align: center;
    // padding: 2vw 0;
    font-size: 4vw;
    font-family: Roboto-Regular;
    font-weight: 400;
    color: hsla(0, 0%, 100%, .7019607843137254);
    margin-top: -2rem;
}
</style>