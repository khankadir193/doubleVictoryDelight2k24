<template>
    <div class="container">
        <div class="arrowHowToPlay">
            <img src="../assets/images/arrow.png" alt="picture-arrow2" />
            <p>Card Mission</p>
            <img src="../assets/images/arrow.png" alt="picture-arrow2" />
        </div>
        <div class="buyBtn">
            <p>Go Buy</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'MissionComp'
}
</script>

<style scoped>
.container {
    border-radius: .4rem;
    width: 90%;
    height: 20vh;
    box-sizing: border-box;
    background: linear-gradient(0deg, #ffedc9, #fdf1e6);
    position: relative;
    margin: 0 auto;
    transform: translateY(1.06667rem);
}

.arrowHowToPlay {
    height: 1vh;
    /* width: 80%; */
    display: flex;
    justify-content: space-between;
    position: relative;
    margin: 0 auto;
    top: 1rem;

    img {
        width: 100%;
    }

    p {
        display: flex;
        width: 100%;
        position: relative;
        top: -1.3rem;
        left: .5rem;
        color: purple;
    }
}

.buyBtn{
    background-image: url('../assets/images/mission-strip.png');
    background-size: 100% 100%;
    background-repeat: no-repeat;
    /* width: 30%; */
    height: 7vh;
    margin-top: 3rem;
    p{
        margin: 0 auto;
        color: white;
        font-weight: bolder;
        text-align: center;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 18px;
    }
}
</style>