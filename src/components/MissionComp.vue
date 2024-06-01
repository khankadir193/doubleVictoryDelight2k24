<template>
    <div class="container">
        <div class="arrowHowToPlay">
            <img src="../assets/images/arrow.png" alt="picture-arrow2" />
            <p>Card Mission</p>
            <img src="../assets/images/arrow.png" alt="picture-arrow2" />
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
</style>