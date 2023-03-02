<template>
    <div id="contactus" class="section">
        <div class="contact-text-img">
            <img class="contact-img" src="../assets/contact-img.svg" alt="">
            <div id="contact-info">

                <div id="email-info">

                    <a href="mailto:info@igen-media.com">

                        <img class="icon" src="../assets/icons/email.png" style="width: 30px;" alt="" srcset="">

                    </a>
                    {{ my_email }}

                </div>

                <div id="insta-info">

                    <a href="https://www.instagram.com/suhaib.smma/" target="_blank">
                        <img class="icon" src="../assets/icons/instagram.png" style="width: 30px;" alt="" srcset="">

                    </a>
                    iGen Media

                </div>
            </div>
        </div>
        <div class="form">
            <h1>Need Help ? Get in touch</h1>
            <input type="text" name="" id="name" placeholder="Name" class="input" v-model="name">
            <input type="email" name="" id="email" placeholder="Email" class="input" v-model="email">
            <textarea name="" id="message" cols="30" rows="10" placeholder="Message" v-model="message"
                class="input"></textarea>

            <a href="#" id="submit-button" :class="{ 'button-inactive': form_not_completed }" @click="send_email">Submit</a>
        </div>




    </div>
</template>
<script>
export default {
    name: 'ContactUs',

    data() {
        return {
            name: '',
            email: '',
            message: '',
            my_email: 'info@igen-media.com',
            contact_msg_success: false
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
                Subject: " Contact igen Media | " + this.name,
                Body: this.message + "\n by " + this.email
            }).then(

                Toastify({
                    text: "Thank You. You'll hear from us soon!",
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
                        background: " linear-gradient(to right, #00b07bec, #3dc960ec)",
                    },
                    onClick: function () { } // Callback after click
                }).showToast(),

                this.name = '',
                this.email = '',
                this.message = ''

            );

        }

    },


    computed: {

        form_not_completed() {
            if (this.name.length == 0 || this.email.length == 0) {
                return true
            } else {
                return false
            }

        }

    }

}
</script>
<style scoped>
#contactus {
    display: flex;
    margin: 0 auto;
    min-height: 70vh;
    justify-content: center;
    align-items: center;
    gap: 7vw;
    padding: 0 5vw 0;
}

.contact-text-img {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 20px;

    width: 50vh;
}

.form {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 20px;
    min-width: 40%;

}

.input {
    width: 100%;
    height: 50px;
    border-bottom-style: solid;
    border-color: black;
    border-bottom-width: 1px;
    color: rgb(22, 22, 22);
    padding-left: 5px;
    font-size: large;
    transition: all 0.2s ease-in-out;
}

.input:focus::placeholder {
    padding-left: 0;
    opacity: 0;
    transition: all 0.2s ease-in-out;

}

.input:focus {
    outline: none;
    border-bottom-style: solid;
    border-bottom-width: 1px;
}

#message {
    height: 200px;
}

#submit-button {
    margin-top: 20px;
    background-color: #4b95e9;
    width: 50%;
    min-height: 50px;
    border-radius: 30px;
    display: flex;
    text-align: center;
    justify-content: center;
    align-items: center;
    transition: all 0.3s ease-in-out;
}

.button-inactive {
    border-style: solid;
    border-width: 1px;
    border-color: black;
    background-color: #9b9b9b00 !important;
    pointer-events: none;
    cursor: default;
    color: rgb(17, 17, 17);

}

#submit-button:hover {
    background-color: #2a7edf;

}

#submit-button:active {
    background-color: #4b95e9;

}

h1 {
    color: #0c4abdd2;
    font-size: 2.2rem;
    margin-bottom: 20px;
    text-align: center;
}

img {
    width: 100%;
    transition: all 0.1s ease-in-out;
}

.icon:hover {
    transform: scale(1.1);
}

.icon {
    transition: all 0.2s ease-in-out;
}

#contact-info {
    margin-top: 30px;
    color: rgb(17, 17, 17);
}

#email-info {

    display: flex;
    gap: 10px;
    align-items: center;
    color: rgb(17, 17, 17);

}

#insta-info {
    margin-top: 10px;
    display: flex;
    gap: 10px;
    align-items: center;
    color: rgb(17, 17, 17);
}

@media all and (max-width: 800px) {
    .contact-img {
        display: none;
    }

    .contact-text-img {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        gap: 20px;
        order: 1;
        width: 50vh;
    }

    .form {
        width: 100%;
    }

    .input {
        width: 80%;
    }

    #contactus {
        flex-direction: column;

    }

    h1 {

        font-size: 1.3rem;

    }


}
</style>