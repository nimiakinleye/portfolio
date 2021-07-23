<template>
  <div>
    <nav>
      <nuxt-link to="/" class="nav-link">Portfolio</nuxt-link>
      <nuxt-link to="/" class="nav-link">Home</nuxt-link>
      <nuxt-link to="/" class="nav-link">Contact Me</nuxt-link>
    </nav>
    <nav :class="{ show: position, hide: !position }" class="fixed_header">
      <nuxt-link to="/" class="nav-link">Portfolio</nuxt-link>
      <nuxt-link to="/" class="nav-link">Home</nuxt-link>
      <nuxt-link to="/" class="nav-link">Contact Me</nuxt-link>
    </nav>
  </div>
</template>

<script>
export default {
  data () {
    return {
      position: ''
    }
  },
  methods : {
    scrollFunc () {
      let position  = window.pageYOffset
      if (position > 150) {
        this.position = true
      } else {
        this.position = false
      }
    }
  },
  mounted () {
    window.addEventListener('scroll', this.scrollFunc)
  }
}
</script>

<style scoped>
nav {
  @apply flex
  divide-x-2
  justify-center
  my-4
  text-xs
  md:text-base;
}
.nav-link {
  @apply uppercase
  px-4
  md:px-8
  font-semibold
  py-2;
}
.fixed_header {
  transition: 1s;
  @apply fixed
  top-0
  w-full
  z-50
  bg-gray-800
  h-14
  py-3
  my-0
  bg-opacity-70;
  -webkit-backdrop-filter: blur(4px);
  backdrop-filter: blur(4px);
}

.show {
  transform: translateY(0);
}

.hide {
  transform: translateY(-300%)
}
</style>