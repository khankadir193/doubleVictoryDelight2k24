<template>
    <div class="howToPlay">
        <div class="arrowHowToPlay">
           <img src="../assets/images/picture_arrow2.png" alt="picture-arrow2"  /> 
           <img src="../assets/images/picture_arrow2.png" alt="picture-arrow2"  /> 
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
    height: 2vh;
    width: 10%;
    display: flex;
    justify-content: space-around;
    /* flex-direction: column; */
    img{
        width: 100%;
    }
}
</style>