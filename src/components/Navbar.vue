<template>
    <div id="navbar" class="z-50 w-full drop-shadow-lg animated fadeInDown fixed top-0 transition duration-300 navbar">
        <div class="flex flex-wrap justify-between items-center p-2 w-full">
            <div class="px-4 w-60 max-w-full">
                <a href="#" class="w-full block py-5">
                <img id="navbar-logo" src="../assets/logo-white.png" alt="logo"/>
                </a>
            </div>

            <div class="invisible flex gap-10 px-10 hover:transition-all lg:visible">
                <button id="aboutbtn" class="underlineOnHover" @click="scrollToElement('about')">Over mij</button>
                <button class="underlineOnHover" href="#home">Projecten</button>
            </div>

            <!-- Add the hamburger menu toggle button -->
            <div class="block lg:hidden">
                <button class="flex items-center px-3 py-2 border rounded text-teal-200 border-teal-400 hover:text-white hover:border-white" @click="toggleMenu">
                <svg class="white fill-current fill-white h-3 w-3" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><title>Menu</title><path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" transition="all 0.3s ease-in-out"/></svg>
                </button>
            </div>
        </div>

        <!-- Add the navbar links for small screens -->
        <div class="w-full block flex-grow lg:hidden lg:items-center lg:w-auto" :class="[showMenu ? '' : 'hidden']">
            <div class="text-sm lg:flex-grow text-right">
                <a href="#" class="block mt-4 lg:inline-block lg:mt-0 mr-4" @click="scrollToElement('about');toggleMenu();">
                    Over mij
                </a>
                <a href="#" class="block mt-4 lg:inline-block lg:mt-0 mr-4" @click="scrollToElement('home');toggleMenu();">
                    Projecten
                </a>
            </div>
        </div>
  </div>

   
</template>

<style scoped>
.navbar{
    @apply text-white;
    --navbar-hover-color: rgb(57, 115, 229);
}

.navbar-scrolled{
    @apply bg-white;
    @apply text-gray-400;
    --navbar-hover-color: black;
}

.underlineOnHover
{
    position: relative;
    transition: 0.3s;
}

.underlineOnHover:before {
  content: "";
  position: absolute;
  width: 100%;
  height: 2px;
  bottom: -10px;
  left: 0;
  background-color: var(--navbar-hover-color);
  visibility: hidden;
  transform: scaleX(0);
  transition: all 0.3s ease-in-out;
}

.underlineOnHover:hover:before {
  visibility: visible;
  transform: scaleX(1);
}

.underlineActive:before{
    content: "";
    position: absolute;
    width: 100%;
    height: 2px;
    bottom: -10px;
    left: 0;
    background-color: rgb(222, 222, 222);
    transform: scaleX(0);
    transition: all 0.3s ease-in-out;
    visibility: visible;
  transform: scaleX(1);
}

.underlineActive:hover:before{
    background-color: var(--navbar-hover-color);
}

button:hover{
    color: var(--navbar-hover-color);
}

.activeText {
    @apply text-black
}
</style>

<script defer>
export default {
    mounted() {
        window.addEventListener("scroll", this.onScroll);
    },
    beforeDestroy() {
        window.removeEventListener("scroll", this.onScroll);
    },
    data(){
        return {
            showMenu: false
        }
    },
    methods: {
        onScroll(e) {
            if (window.scrollY > 10) {
                this.showScrollingNavbar();
            } 
            else {
                this.showLandingPageNavbar();
            }

            const sections = document.querySelectorAll("section[id]");
            sections.forEach(current => {
                const sectionHeight = current.offsetHeight;
                const sectionTop = current.offsetTop - 100;
                let sectionId = current.getAttribute("id");
                
                if (scrollY > sectionTop && scrollY <= sectionTop + sectionHeight){
                    // document.getElementById(sectionId + "btn").classList.add("underlineActive");
                    document.getElementById(sectionId + "btn").classList.add("activeText");
                } 
                else {
                    // document.getElementById(sectionId + "btn").classList.remove("underlineActive");
                    document.getElementById(sectionId + "btn").classList.remove("activeText");
                }
            });
        },
        showScrollingNavbar(){
                document.getElementById("navbar-logo").src = "src/assets/logo.png";
                document.getElementById("navbar").classList.remove('navbar');
                document.getElementById("navbar").classList.add('navbar-scrolled');
        },
        showLandingPageNavbar(){
                document.getElementById("navbar-logo").src = "src/assets/logo-white.png";
                document.getElementById("navbar").classList.remove('navbar-scrolled');
                document.getElementById("navbar").classList.add('navbar');

                document.querySelector(':root').style.setProperty('--navbar-text-color', 'black');
        },
        scrollToElement(elementId) {
            const yOffset = -50; 
            const element = document.getElementById(elementId);
            const y = element.getBoundingClientRect().top + window.pageYOffset + yOffset;

            window.scrollTo({top: y, behavior: 'smooth'});
        },
        toggleMenu() {
            this.showMenu = !this.showMenu
        }
    }
};
</script>