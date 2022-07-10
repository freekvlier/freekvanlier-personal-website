<template>
    <div id="navbar" class="z-50 w-full drop-shadow-lg animated fadeInDown fixed top-0 transition duration-300">
        <div class="container flex flex-wrap justify-between items-center p-2">
            <div class="px-4 w-60 max-w-full">
                <a href="#" class="w-full block py-5">
                <img id="navbar-logo" src="../assets/logo-white.png" alt="logo"/>
                </a>
            </div>

            <div>
                <ul class="flex gap-10 px-40">
                    <li class="relative group">
                        <a href="#home" class="font-bold">
                            <!-- Home -->
                        </a>
                    </li>
                </ul>
            </div>

        </div>
    </div>
</template>

<style scoped>

</style>

<script defer>
window.onscroll = () => {
    if (window.scrollY > 10) {
        document.getElementById("navbar").classList.add('bg-white');
        document.getElementById("navbar-logo").src = "src/assets/logo.png";
    } else {
        document.getElementById("navbar").classList.remove('bg-white');
        document.getElementById("navbar-logo").src = "src/assets/logo-white.png";
    }
};


/*
let offset = nav.getBoundingClientRect();

document.onscroll = function (e) {
    scrollStart = e.target.scrollingElement.scrollTop;
    if (scrollStart > offset.top) {
        console.log('test');
        //nav.style.background-color, rgba(34,34,34,0.9);
    } else {
        //nav.style.background-color = "transparent";
    }
};
*/
</script>