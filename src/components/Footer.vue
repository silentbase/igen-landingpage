<template>
    <div id="footer">
        <div id="footer-container">
            <div style="display: flex; flex-direction: column; align-items: center;">
                <h1>Get the latest updates and special offers</h1>
                <h1 class="footer_text_2">Subsribe to our newsletter now !</h1>


            </div>

            <div id="newsletter-container">
                <div id="input-container">
                    <input type="email" name="" id="email" v-model="input">

                    <a id="newsletter-button" href="#" @click="send_email">Subscribe</a>
                </div>

            </div>

            <div id="footer-info">
                <h2>iGen Media</h2> <br>
                <p>Terms & Conditions | Privacy Policy | Disclaimer</p>
            </div>
        </div>

    </div>
</template>
<script>

import { useToast } from "vue-toastification";

export default {

    data() {
        return {
            input: '',
            contact_msg_success: true,
            my_email: 'info@igen-media.com',
        }
    },

    methods: {
        send_email: function () {

            Email.send({
                Host: "smtp.elasticemail.com",
                Username: "ademsmm2000@gmail.com",
                Password: "70A07EEA72A9B66E0C4C7A0F9103573D39AE",
                To: this.my_email,
                From: 'ademsmm2000@gmail.com',
                Subject: " Newsletter igen Media | ",
                Body: 'New Newsletter sub: ' + this.input
            }).then(

                this.contact_msg_success = true,
                this.input = '',
                Toastify({
                    text: "Subscribed Succesfully",
                    className: "info",
                    duration: 7000,
                    newWindow: true,
                    close: true,
                    gravity: "top", // `top` or `bottom`
                    position: "center", // `left`, `center` or `right`
                    stopOnFocus: true, // Prevents dismissing of toast on hover
                    style: {
                        background: "linear-gradient(to right, #00b09b, #96c93d)",
                        padding: "70px;",
                        background:" linear-gradient(to right, #00b07bec, #3dc960ec)",
                },
                    onClick: function () { } // Callback after click
                }).showToast()

            );

    }

},

}
</script>
<style scoped>
#footer {
    background: radial-gradient(rgb(58, 58, 58), rgb(63, 63, 63));
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 10vh;
}

#footer-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-around;
    min-height: 50vh;


    gap: 20%;
    padding: 20px;
}

#input-container {
    display: flex;
    justify-content: space-between;

    align-items: center;
    background-color: rgb(255, 255, 255);
    width: 70vw;
    border-radius: 20px;
}

#email {
    background-color: rgba(197, 28, 28, 0);
    outline: none;
    color: rgb(26, 26, 26);

    min-height: 50px;
    width: 90%;
    font-size: 1.1rem;
    padding: 0px 20px 0px;
}

input:-webkit-autofill {
    color: rgb(26, 26, 26) !important;
    background-color: red !important;
    border-radius: 20px !important;
}

#email:-webkit-autofill {}

#newsletter-button {
    font-size: 1.1rem;
    color: rgb(26, 26, 26);
    transition: all 0.2s ease-in-out;
    padding-right: 20px;
    transition: transform 0.1s ease-in-out;
}

#newsletter-button:hover {
    transform: scale(1.08);
    transition: transform 0.1s ease-in-out;
    color: rgb(42, 54, 233);
}


#footer-info {
    text-align: center;
}

h2 {
    font-size: 1.1rem;
    color: rgb(0, 153, 255);
}

h1 {
    font-size: 2rem;

}

.footer_text_2 {
    font-size: 1.4rem;
    color: rgb(0, 153, 255);
    margin-top: 10px;
}

@media all and (max-width: 800px) {

    h1 {
        font-size: 4vw;
        text-align: center;
    }

    .footer_text_2 {
        display: none;
    }
}
</style>