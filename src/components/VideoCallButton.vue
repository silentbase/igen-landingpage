<template>
    <div>
        <a id="button" type="button" value="Schedule A Free Call Today" :style="styleProp" href="https://calendly.com/igenmedia/30min" target="_blank"
        >Schedule A Free Audit Call Today</a>
    </div>
</template>

<script>
export default {
    props: {
        styleProp: String,
        textProp: String
    },
    name: 'VideoCallButton',

    data() {
        return {
            width: this.widthProp
        }
    }


}
</script>

<style>
#button {
    min-height: 70px;
    border-radius: 40px;
    background-color: #4b95e9;
    border-width: 1px;
    border-color: rgb(61, 61, 61);
    font-weight: 700;
    font-size: 22px;
    transition: all 0.1s ease-in-out;
    color: rgb(20, 20, 20);
    
    display: flex;
    text-align: center;
    justify-content: center;
    align-items: center;


}

#button:hover {
    background-color: rgb(49, 139, 241);

    transform: scale(1.05);
    transition: all 0.1s ease-in-out;
    cursor: pointer;
}

#button:active {
    background-color: rgb(103, 168, 241);
    animation: none;
}

@media all and (min-width: 800px) and (max-width: 1200px) {

    #button {
        max-width: 35vw;
        font-size: 2vw;
        min-height: 7vh;


    }
}


@media all and (max-width: 800px) {
    #button {
        max-width: 50vw;
        min-height: 7vh;
        font-size: 4vw;
        position: relative;
        
        padding: 20px;
    }
}




@keyframes button-anime {

    0% {
        background-color: rgb(75, 149, 233);
        transform: scale(1);
    }

    50% {
        background-color: rgb(49, 171, 241);
        transform: scale(1.01);
    }

    100% {
        background-color: rgb(75, 149, 233);
        transform: scale(1);
    }


}
</style>