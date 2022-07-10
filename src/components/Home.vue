<template lang="">
    <div class="content h-screen text-white flex flex-col items-center justify-center text-center text-lg">
        <span class="text-5xl pb-2">
            Ik ben <span class="text-blue-500"> Freek van Lier </span>
        </span>
        <span>
            Een <span class="font-bold">Full-stack Developer</span> met kennis <br>
            uit alle stadia van softwareontwikkeling
        </span>
    </div>
</template>

<script>
export default {
    
}
</script>

<style scoped>

.content{
    /* background-image: linear-gradient(rgba(0,0,0,), url("../assets/me.jpg")); */
    background: linear-gradient(rgba(0, 0, 0, 0.8), rgba(0, 0, 0, 0.8)),url("../assets/me.png") no-repeat center center; /* The least supported option. */;
    background-size: cover;
}


</style>