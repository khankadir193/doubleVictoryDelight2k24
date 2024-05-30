<template>
    <div class="howToPlay">
        <div class="arrowHowToPlay">
           <img src="../assets/images/arrow.png" alt="picture-arrow2"  /> 
           <p>How To Play</p>
           <img src="../assets/images/arrow.png" alt="picture-arrow2"  /> 
        </div>
    </div>
</template>

<script>
export default {
    name: 'HowToPlayComp',
}
</script>

<style scoped>
.howToPlay{
    background-image: url('../assets/images/howToPlayBg.png');
    background-size: 100% 100%;
    width: 90%;
    height: 40vh;
    margin: 0 auto;
}
.arrowHowToPlay{
    height: 1vh;
    /* width: 80%; */
    display: flex;
    justify-content: space-between;
    position: relative;
    margin: 0 auto;
    top: 1rem;
    img{
        width: 100%;
    }
    p{
        display: flex;
        width: 100%;
        position: relative;
        top: -1.3rem;
        left: .5rem;
        color: purple;
    }
}
</style>