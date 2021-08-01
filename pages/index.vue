<template>
  <div>
		<Header id="home"/>
    <Banner />
    <Benefits />
    <Portfolio id="portfolio"/>
	</div>
</template>

<script>
import Header from '~/components/Header.vue'
import Banner from '~/components/Banner.vue'
import Benefits from '~/components/Benefits.vue'
import Portfolio from '~/components/Portfolio.vue'
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
</style>