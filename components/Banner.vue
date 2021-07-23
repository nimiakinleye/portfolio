<template>
  <div class="banner">
    <Navbar />
    <div class="b_ner container">
      <div class="caption" data-aos="flip-up" data-aos-duration="1000">
        <div id="star">
          <img src="~/assets/star.svg" alt="" />
        </div>
        <div id="whoosh">
          <img src="~/assets/whoosh.svg" alt="" />
        </div>
        <p class="name">toluwanimi <span class="font-bold">akinleye</span></p>
        <p class="role">front-end web developer</p>
        <p class="introduction">
          Hi there. Welcome, My name is Toluwanimi. I'm an experienced Front-end
          web developer with in-depth knowledge in JavaScript front-end
          frameworks (Vue.js and React.js)
        </p>
        <button>HIRE ME</button>
      </div>
      <BannerVector />
    </div>
  </div>
</template>

<script>
import aosMixin from '~/mixins/aos'
import Navbar from '~/components/Navbar.vue'
import BannerVector from '~/components/BannerVector.vue'
export default {
  components: {
    Navbar,
    BannerVector,
  },
  mixins: [aosMixin],
}
</script>

<style>
.banner {
  background-image: url('~/assets/bg_lines.svg');
  background-repeat: no-repeat;
  @apply bg-gray-700
  py-12
  text-white;
}

.banner .b_ner {
  @apply flex
  flex-col-reverse
  items-center
  md:flex-row
  md:justify-between;
}

.container {
  @apply mx-auto;
}

.banner .caption {
  @apply max-w-sm
  text-center
  md:text-left
  px-2
  relative;
}

#star {
  @apply absolute
  -top-24
  hidden
  md:inline;
}

#whoosh {
  @apply absolute
  bottom-0
  -right-28
  hidden
  md:inline
}

.banner .caption .name {
  @apply uppercase
  font-light
  text-3xl;
}

.banner .caption .role {
  @apply uppercase
  font-bold
  text-xl
  my-1.5;
}

.banner .caption .introduction {
  @apply text-sm
  font-thin
  my-1.5;
}

.banner button {
  @apply bg-white
  text-gray-700
  py-1
  px-3
  rounded-md;
}
</style>