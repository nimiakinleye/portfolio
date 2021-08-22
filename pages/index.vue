<template>
  <div>
		<Header id="home"/>
    <Banner />
    <Benefits />
    <Portfolio class="pt-16" id="portfolio"/>
    <Contact class="pt-16 mt-48 lg:mt-0" id="contact"/>
	</div>
</template>

<script>
import Header from '~/components/Header.vue'
import Banner from '~/components/Banner.vue'
import Benefits from '~/components/Benefits.vue'
import Portfolio from '~/components/Portfolio.vue'
import Contact from '~/components/Contact.vue'
export default {
  head () {
    return {
      title: 'NimiAkinleye'
    }
  },
  components: {
    Header,
    Banner,
    Benefits,
    Portfolio,
    Contact,
  },
  data () {
    return {
      clicked: false
    }
  },
  methods: {
    getHash() {
      // if (window.pageYOffset > 1500 && !this.clicked) {
      //   window.location.hash = 'portfolio'
      // } else {
      //   window.location.hash = null
      // }
      window.location.hash = null
      // console.log('scrolling')
    },
    setClick() {
      this.clicked = true
    }
  },
  mounted () {
    window.addEventListener('scroll', this.getHash)
    // window.addEventListener('click', this.setClick)
  }
}
</script>

<style>
html {
  scroll-behavior: smooth;
}

.container {
  @apply w-full
}
</style>