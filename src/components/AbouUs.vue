<template >
    <div id="aboutus" class="section">

        <img id="aboutus-img" src="../assets/rocket.svg" alt="" />
        <div id="aboutustext">
            <h2>
                TikTok Marketing Mastery: <br />
                Viral Campaigns and Proven Results.
            </h2>
            <br />
            <p>
                Our team of experts is passionate about creating viral and effective
                marketing campaigns that drive real results. We know that the TikTok
                algorithms and trends are always changing and we make sure to always
                be on top of the latest updates. <br />
                <br />
                Whether you're looking to increase brand awareness, drive website
                traffic, or boost sales, our team has the skills and expertise to help
                you achieve your goals.
            </p>

        </div>
        <VideoCallButton id="callbutton" styleProp="width: 450px;" textProp="Schedule A Free Call Today">
        </VideoCallButton>


    </div>
</template>
<script>
import VideoCallButton from './VideoCallButton.vue';
export default {
    components: {
        VideoCallButton
    }
}
</script>
<style scoped>
#aboutus {
    display: flex;
    align-items: center;
    justify-content: center;

    flex-direction: column;
    width: 80vw;
    margin: 0 auto;
}

#aboutustext h2 {

    color: #0c4abd;
    font-size: 35px;
}

#aboutustext p {


    color: hsl(0, 0%, 7%);
    font-size: 1.7rem;
}

#aboutustext {
    display: flex;
    flex-direction: column;
    max-width: 80%;

    min-height: 500px;
    padding: 50px;
}

#callbutton {


    flex: 10;
}

#aboutus img {
    width: 30%;
    height: auto;
    transform: rotateZ(25deg);
}

@media all and (max-width: 800px) {
    #aboutustext h2 {

        color: #0c4abd;
        font-size: 6vw;
        text-align: center;
    }

    #aboutustext p {

        text-align: center;
        color: hsl(0, 0%, 7%);
        font-size: 4vw;
    }

    #aboutustext {
    padding: 0;
    padding-top: 50px;
    padding-bottom: 50px;
}
#aboutus img {
    width: 70%;
    height: auto;
    transform: rotateZ(25deg) translateX(-10px);
}
}
</style>