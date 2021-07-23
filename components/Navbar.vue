<template>
  <div>
    <nav>
      <div @click="navigate('portfolio')" class="nav-link">Portfolio</div>
      <div @click="navigate('home')" class="nav-link">Home</div>
      <div class="nav-link">Contact Me</div>
    </nav>
    <nav :class="{ show: position, hide: !position }" class="fixed_header">
      <div @click="navigate('portfolio')" class="nav-link">Portfolio</div>
      <div @click="navigate('home')" class="nav-link">Home</div>
      <div class="nav-link">Contact Me</div>
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
    },
    navigate (data) {
      window.location.hash = data
      console.log(data)
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
  transition: .5s;
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