<template>
  <div id="app">
    <NavBar v-if="!mobileView" />
    <MobileNav v-if="mobileView" />
    <Header />
    <Features />
    <Extensions />
    <Faq />
    <Contact />
    <Footer />
  </div>
</template>

<script>
import NavBar from './components/NavBar.vue'
import MobileNav from '@/components/NavBarMobile.vue'
import Header from './components/Header.vue'
import Features from '@/components/Features.vue'
import Extensions from '@/components/Extensions.vue'
import Faq from '@/components/Faq.vue'
import Contact from '@/components/Contact.vue'
import Footer from '@/components/Footer.vue'

export default {
  name: 'App',
  components: {
    NavBar,
    MobileNav,
    Header,
    Features,
    Extensions,
    Faq,
    Contact,
    Footer
  },
   data() {
    return {
        mobileView: false,
    }
  },
  methods: {
    handleView() {
      this.mobileView = window.innerWidth <= 965;
    }
  },
  created() {
    this.handleView();
      window.addEventListener('resize', this.handleView);
  }
}
</script>

<style lang="scss">
  @import url('https://fonts.googleapis.com/css2?family=Rubik:wght@400;500&display=swap');

    $SoftBlue: hsl(231, 69%, 60%);
    $SoftRed: hsl(0, 94%, 66%);
    $DarkBlue: hsl(229, 31%, 21%);
    $LightBlue: hsl(229, 8%, 60%);

  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    scroll-behavior: smooth;
  }
  #app {
    font-family: 'Rubik', sans-serif;
  }
  .btn {
    text-decoration: none;
    color: #fff;
    background-color: $SoftBlue;
    padding: 10px 30px;
    border-radius: 5px;
    font-weight: 600;
    -webkit-box-shadow: 0px 2px 30px -8px rgba(148,148,148,1);
    box-shadow: 0px 2px 30px -8px rgba(148,148,148,1);
    outline: none;
    cursor: pointer;
    border: 2px solid transparent;
    transition: ease .5s;

    &:active {
      transform: scale(.98);
    }
  }
</style>
