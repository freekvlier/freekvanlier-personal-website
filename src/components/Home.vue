<template lang="">
    <div class="home h-screen text-white flex flex-col items-center justify-center text-center text-lg">
        <span class="text-5xl pb-2">
            Ik ben <span class="text-blue-500"> Freek van Lier </span>
        </span>
        <span>
            <span class="font-bold">Software Engineering Student </span> bij Fontys Eindhoven <br>
        </span>
    </div>
    <div class="arrow">
            <span class="arrowSpan"></span>
            <span class="arrowSpan"></span>
            <span class="arrowSpan"></span>
    </div>
    
</template>

<script>
export default {
    mounted() {
    },
    beforeDestroy() {
        window.removeEventListener("scroll", this.onScroll);
    },
    methods: {

    }
};
</script>

<style scoped>
.home{
    /* background-image: linear-gradient(rgba(0,0,0,), url("../assets/me.jpg")); */
    background: linear-gradient(rgba(0, 0, 0, 0.8), rgba(0, 0, 0, 0.8)),url("../assets/meV3.png") no-repeat center center; /* The least supported option. */;
    background-size: cover;
    background-position: 90% 90%;
}

.arrow{
    position: absolute;
    top: 90%;
    left: 50%;
    transform: translate(-50%,-50%);
}

.arrowSpan{
    display: block;
    width: 30px;
    height: 30px;
    border-bottom: 5px solid #ffffffc0;
    border-right: 5px solid #ffffffc0;
    transform: rotate(45deg);
    margin: -10px;
    opacity: 0;
    animation: animate 2s 1s;
    /* animation-delay: 2s; */
}

.arrowSpan:nth-child(2){
    animation-delay: 0.8s;
}

.arrowSpan:nth-child(3){
    animation-delay: 0.6s;
}

@keyframes animate {
    0%{
        opacity: 0;
        transform: rotate(45deg) translate(-20px,-20px);
    }
    50%{
        opacity: 1;
    }
    100%{
        opacity: 0;
        transform: rotate(45deg) translate(20px,20px);
    }
}
</style>
