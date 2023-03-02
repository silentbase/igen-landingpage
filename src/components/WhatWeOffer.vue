<template >
    <div id="whatwedo" class="section">


        <div id="whatwedo-container">
            <h2 id="whatwedo-title" style="margin: 0 auto;">What We Offer</h2>
            <div class="whatwedo-elements" id="paidad">
                <img src="../assets/paid-ad.svg" alt="" srcset="">
                <div id="paidad-text">
                    <h2>Paid Advertisement</h2>
                    <p>One of the standout features of TikTok advertising is the
                        platform's use of creative and interactive ads, like in-feed
                        native videos, branded hashtags, and branded lenses, that truly
                        engage users. This allows your brand to capture their attention
                        and stand out in their feed!</p>
                </div>
            </div>
            <div class="whatwedo-elements" id="influencer">

                <div id="influencer-text">
                    <h2>Influencer Marketing</h2>
                    <p>Let the power of influence work for you. Influencers have built a
                        following of engaged and dedicated fans who trust their
                        recommendations. Partnering with an influencer can help you tap
                        into this captive audience and skyrocket your sales.</p>
                </div>
                <img src="../assets/influencer.svg" alt="" srcset="">
            </div>
        </div>

        <VideoCallButton id="callbutton" styleProp="width: 450px;" textProp="Schedule A Free Call Today"></VideoCallButton>


    </div>
</template>
<script>

import VideoCallButton from './VideoCallButton.vue';

export default {
    name: 'WhatWeDo',
    components: {
        VideoCallButton
    }

}
</script>
<style scoped>
#whatwedo {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;

}

#whatwedo-title {
    color: #3d3d3d77;
    font-size: 3rem;
}

#whatwedo-container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 3%;
    width: 76vw;

}

.whatwedo-elements {
    display: flex;
    justify-content: center;
    gap: 10%;
    align-items: center;
}

#paidad-text {}

img {
    width: 30%;

}

h2 {
    font-size: 1.7rem;
    color: #0c4abd;
    margin-bottom: 15px;

}

p {
    color: hsl(0, 0%, 7%);
    font-size: 1.5rem;
}

@media all and (max-width: 800px) {

    img {
        width: 70%;

    }

    .whatwedo-elements {
        flex-direction: column;
        gap: 5vh;
    }

    #whatwedo-container {
        gap: 5vh;
    }

    #influencer {
        
    }

    #whatwedo-title {
        color: #3d3d3d77;
        font-size: 1.8rem;
    }

    h2 {
        font-size: 6vw;
        color: #0c4abd;
        text-align: center;

    }

    p {
        color: hsl(0, 0%, 7%);
        font-size: 4vw;
        text-align: center;
    }

    #influencer-text{
        order: 1;
    }

    #callbutton{
        margin-top: 50px;
    }
}</style>