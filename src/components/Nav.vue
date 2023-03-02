<template>
    <div id="navbar" class="">
        <h2 class="logo">Buzz Media</h2>
        <nav :class="{ 'burger-menu-active': mobileNavIsActive }">
            <a href="#aboutus">About Us</a>
            <a href="#whatwedo">What We Do</a>
            <a href="#testimonials">Testimonials</a>
        </nav>

        <div id="burger-menu" @click="
            mobileNavIsActive == false
                ? (mobileNavIsActive = true)
                : (mobileNavIsActive = false)
        ">
            <div :class="{
                'burger-x1': mobileNavIsActive,
            }" class="burgerline"></div>
            <div :class="{
                'burger-x2': mobileNavIsActive,

            }" class="burgerline"></div>
            <div :class="{
                'burger-x3': mobileNavIsActive,

            }" class="burgerline"></div>
        </div>

    </div>
</template>
  
<script>
export default {
    data() {
        return {
            mobileNavIsActive: false,
        };
    },
};
</script>
  
<style scoped>
#navbar {
    width: 100%;
    position: sticky;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 2rem 0rem 2rem;
    background-color: rgba(255, 0, 0, 0);
    z-index: 999;
}

#burger-menu {
    display: none;
    position: relative;
    right: 1%;
    cursor: pointer;
}

.burgerline {
    height: 3px;
    width: 30px;
    margin: 5px;
    background: rgb(236, 236, 236);
    transition: all 0.2s ease-in-out;
}

.logo {
    position: relative;
    left: 7%;
    font-size: 1.5rem;
}

nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 25rem;
    position: relative;
    right: 7%;
}

nav a {
    text-decoration: none;
    font-size: 1rem;
}

a:hover {
    transform: scale(1.06);
    color: #f079ea;
    transition: all ease-in-out 0.1s;
}

@media all and (max-width: 800px) {
    #burger-menu {
        display: block;
    }

    .burger-menu-active {
        transform: translateY(0%);

    }

    .burger-x1 {
        transform: translateY(8px) rotate(45deg);
        transition: all 0.2s ease-in-out;
    }

    .burger-x3 {
        transform: translateY(-8px) rotate(-45deg);
        transition: all 0.2s ease-in-out;
    }

    .burger-x2 {
        transition: all 0.1s ease-in-out;
        opacity: 0;
    }

    #navbar {
        background-color: rgba(49, 49, 49, 0.973);
        position: fixed;

    }

    nav {
        position: fixed;
        right: 0;
        top: 10.8vh;
        height: 100vh;
        width: 70%;
        background-color: #131313;
        flex-direction: column;
        justify-content: space-evenly;
        background-color: #1b1b1bfa;
        transform: translateX(100%);
        transition: transform 0.2s ease-in-out;
        z-index: 999;
        overflow: hidden;
    }

    nav a {
        color: rgb(245, 245, 245);
        transition: all 0.1s ease-in-out;
        border-width: 1px;
        border-radius: 7%;
        border-style: none;
        border-color: rgb(240, 121, 234);
        padding: 25px 2rem 25px;
    }
    
    a:hover{
       color: rgb(240, 121, 234);
       border-style: solid;
       
       transition: all 0.1s ease-in-out;
    }

    @keyframes burger-animation {
        0% {
            transform: translateY(0px) rotateZ(0deg);
        }

        100% {
            transform: translateY(0px) rotateZ(0deg);
        }
    }
}
</style>