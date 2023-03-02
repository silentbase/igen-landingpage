
<template>

  <div id="app">

    <Hero/>
    <AboutUs/>
    <WhatWeOffer/>
    <WhyUs/>
    <ContactUs/>
    <Footer/>


  </div>


</template>


<script setup>

import Hero from './components/Hero.vue'
import WhyUs from './components/WhyUs.vue'
import WhatWeOffer from './components/WhatWeOffer.vue'
import AboutUs from './components/AbouUs.vue'
import ContactUs from './components/ContactUs.vue'
import Footer from './components/Footer.vue'







</script>

<style>

@import url("https://fonts.googleapis.com/css2?family=Montserrat&display=swap");

*{
  font-family: 'Montserrat';
  font-weight: 600;
  color: rgb(236, 236, 236);
  margin: 0;
  padding: 0;
  box-sizing: border-box;
 
}

#app{
  overflow-x: hidden;
}

</style>

<style >

  .section  {
    padding-bottom: 10vh;
  }

</style>
