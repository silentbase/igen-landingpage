<template>
    <div class="section">
        <section class="py-12 bg-white sm:py-16 lg:py-20 ">
            <div class="px-4 mx-auto  sm:px-6 lg:px-8 whyus-width">
                <div class="text-center">
                    <h2 class="text-3xl font-bold leading-tight text-gray-900 sm:text-4xl xl:text-5xl font-pj whyus-title">Why Choose Our Agency</h2>
                </div>

                <div
                    class="grid grid-cols-1 mt-10 text-center sm:mt-16 sm:grid-cols-1 sm:gap-x-12 gap-y-12 md:grid-cols-3 md:gap-40 xl:mt-24 whyus">
                    <div class="grid-elements">
                        <img src="../assets/icons/guarantee.png" width="130px" alt="" srcset="">
                        <h3 class="mt-12 text-xl font-bold text-gray-900 font-pj">High Quality</h3>
                        <p class="mt-5 text-base text-gray-600 font-pj">Committed to providing campaigns that are both reliable and of the highest quality, every time.</p>
                    </div>

                    <div class="grid-elements">
                        <img src="../assets/icons/play.png" width="130px" alt="" srcset="">
                        <h3 class="mt-12 text-xl font-bold text-gray-900 font-pj">Content Creation</h3>
                        <p class="mt-5 text-base text-gray-600 font-pj">Missing a video? No problem! We've got you covered with content that will capture the attention of your potential customers.</p>
                    </div>

                    <div class="grid-elements">
                        <img src="../assets/icons/celebrity.png" width="130px" alt="" srcset="">
                        <h3 class="mt-12 text-xl font-bold text-gray-900 font-pj">Picking the right influencers</h3>
                        <p class="mt-5 text-base text-gray-600 font-pj">Selecting TikTok influencers who align well with your brand and are known for their reliability and precision.</p>
                    </div>

                   

                  

                    


                </div>
                <div id="button-div">
                    <VideoCallButton id="callbutton" styleProp="width: 450px;" textProp="Schedule A Free Call Today"></VideoCallButton>
                </div>
            </div>


        </section>




    </div>
</template>
    
<script>

import VideoCallButton from './VideoCallButton.vue';

export default {
    name: 'WhateWeDo',
    components: {
        VideoCallButton
    },

}
</script>
    
<style scoped>
.grid-elements {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
}

.test2 {}

.whyus div {

    border: none;
}

section {
    display: flex;
    justify-content: center;
    background: radial-gradient(rgb(58, 58, 58),rgb(63, 63, 63));
    padding-bottom: 3vh;
}

.whyus-width {
    width: 70vw;
    margin: 0;
}

.whyus-title{
    color: #f0f0f0;
    font-size: 3rem;
}

#callbutton {
    padding: 0px;
    margin: 0px;

}

#button-div {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 7%;
}

p{
    font-size: 1.3rem;
    font-weight: 500;
    color: rgb(255, 255, 255);
}

h3 {
    color: #4ecdf3;
}

#callbutton{
        margin-top: 50px;
    }

@media all and (max-width: 800px) {

    .whyus-title{
        font-size: 1.5rem;
    }

    #callbutton{
        margin-top: 50px;
    }

    img{
        width: 100px;
    }

    p{
        font-size: 4vw;
    }
    

}
</style>