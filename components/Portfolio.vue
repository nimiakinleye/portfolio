<template>
  <div class="portfolio">
    <div class="lg:grid grid-cols-4">
      <div class="max-w-sm col-start-1 col-end-2" data-aos="fade-right">
        <div class="flex items-center mb-3">
          <div class="bar"></div>
          <h4 class="title">Past Projects</h4>
        </div>
        <p class="caption">
          These are projects that I've had the opportunity to be a part of, and
          they've also helped me become a better developer. As a result, I'll do
          a better job on your project.
        </p>
      </div>
    </div>
    <div class="lg:grid grid-cols-4 jobs">
      <div class="col-start-1 col-end-3 bg-black bg-opacity-0"></div>
      <div class="col-start-3 col-end-5" data-aos="zoom-in">
        <Jobs />
        <Jobs />
        <Jobs />
        <Jobs />
        <Jobs />
      </div>
    </div>
  </div>
</template>

<script>
import aosMixin from '~/mixins/aos'
import Jobs from '~/components/Jobs.vue'
export default {
  components: {
    Jobs,
  },
  mixins: [aosMixin]
}
</script>

<style scoped>
.portfolio {
  background-image: url(~/assets/portfolio.svg);
  background-position: top;
  background-repeat: no-repeat;
  background-size: contain;
  @apply h-96
  relative
  my-10;
}

.bar {
  @apply w-20
  h-2
  mr-2
  rounded-r-full;
  background-color: #374151;
}

.title {
  @apply font-bold
  text-2xl;
  color: #374151;
}

.caption {
  @apply lg:ml-12
  ml-auto
  px-2
  pb-2;
}
.sticky {
  position: -webkit-sticky;
  position: sticky;
  top: 50px;
}

.jobs {
  @apply lg:mr-24
  h-96
  overflow-auto
  absolute
  lg:top-0;
  scrollbar-width: none;
  -ms-overflow-style: none;
}

.jobs::-webkit-scrollbar {
  display: none;
}
</style>