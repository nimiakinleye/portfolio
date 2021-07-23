<template>
  <div>
		<Header />
    <Banner />
    <Benefits />
    <Portfolio />
	</div>
</template>

<script>
import Header from '~/components/Header.vue'
import Banner from '~/components/Banner.vue'
import Benefits from '~/components/Benefits.vue'
import Portfolio from '~/components/Portfolio.vue'
export default {
  components: {
    Header,
    Banner,
    Benefits,
    Portfolio,
  },
}
</script>

<style>
</style>