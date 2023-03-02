<template >
    <div id="hero" class="section">
        <h1 class="logo" style="font-size: 1.5rem; "><a href="">iGen Media</a></h1>

        <div id="hero-container">
            <div id="tiktok-svg">
                <TiktokSvg id="svg" />
            </div>

            <div id="text-button-container">
                <div id="hero-text">
                    <h1 id="title">The Beat Of Your Business</h1>
                    <br />
                    <h2 id="first-text">
                        We at iGen Media focus on unlocking the Power of TikTok for Your
                        E-Commerce Business. Drive Sales and Build Trust with our
                        exceptional Marketing Campaigns.
                    </h2>
                    <br />
                    <p id="second-text">
                        Don't settle for mediocre branding services. Choose a professional
                        team that is focused on delivering expetional ROI to your e-commerce
                        business.
                    </p>

                </div>
                <VideoCallButton id="callbutton" styleProp="width: 450px;" textProp="Schedule A Free Call Today"></VideoCallButton>
            </div>

        </div>
    </div>
</template>
<script>

import Nav from './Nav.vue'
import TiktokSvg from './svg-components/TiktokSvg.vue'
import VideoCallButton from './VideoCallButton.vue';

export default {

    components: {
        Nav,
        TiktokSvg,
        VideoCallButton
    }

}
</script>
<style scoped>
.logo {
    position: relative;
    top: 4vh;
    left: 7vh;
}

#hero {
    background-image: radial-gradient(at 80% 50%,
            rgba(17, 17, 17, 0.712),
            rgba(15, 15, 15, 0.712)),
        url("../assets/hero_bg.png");

    background-size: cover;
    min-height: 90vh;
    margin-bottom: 10vh;
    padding-bottom: 3vh;
}

#hero-container {
    padding-top: 5vh;
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 4vw;
}

#text-button-container {

    min-height: 60vh;
    display: flex;
    flex-direction: column;
    justify-content: end;
    align-items: start;

}

#hero-text {

    max-width: 40vw;
    flex: 0.7;
    display: flex;
    flex-direction: column;
    justify-content: center;

}


#title {
    font-size: 2rem;
}

#first-text {
    font-size: 2.2rem;
    color: rgb(84, 148, 221);
    text-shadow: -1px -1px 0 #272727, 1px -1px 0 #272727, -1px 1px 0 #272727,
        1px 1px 0 #272727;
}

#second-text {
    font-size: 1.5rem;
}

#hero-container {
    gap: 0
}

#callbutton {
    padding-top: 3vh;
}

@media all and (min-width: 800px) and (max-width: 1500px) {

    #title {
        font-size: 1.5rem;
    }

    #first-text {
        font-size: 1.7rem;
        color: rgb(84, 148, 221);
    }

    #second-text {
        font-size: 1.2rem;
    }

    #callbutton {
        margin-top: 0;
    }

    #text-button-container {
        padding-right: 10%;


    }


}

@media all and (max-width: 800px) {

    #hero-container {
        flex-direction: column;
        justify-content: center;
        align-items: center;
        gap: 0;
        padding-bottom: 3vh;
        padding-top: 0;
    }

    #text-button-container {
        align-items: center;

    }

    #svg {
        max-width: 100vw;
    }

    #hero-text {

        max-width: 70vw;
        margin: 5vw 5vw 0vw;
        text-align: center;
    }

    #title {
        font-size: 9vw;
    }

    #first-text {
        font-size: 6vw;
        color: rgb(84, 148, 221);
    }

    #second-text {
        font-size: 5vw;
    }

    .logo {
        position: relative;
        top: 3vh;
        left: 4vh;
    }

    #svg{
        object-fit: cover;
        height: 50vh;
    }

}
</style>