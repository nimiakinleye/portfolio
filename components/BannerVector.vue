<template>
  <div class="vector" data-aos="zoom-in" data-aos-duration="1000">
    <div class="dev"><img src="~/assets/banner_vector.svg" alt="" /></div>
    <div class="vue_icon icon">
      <img src="~/assets/vue.svg" alt="" />
    </div>
    <div class="js_icon icon">
      <img src="~/assets/js.svg" alt="" />
    </div>
    <div class="nuxt_icon icon">
      <img src="~/assets/nuxt.svg" alt="" />
    </div>
    <div class="css_icon icon">
      <img src="~/assets/css.svg" alt="" />
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.vector {
  @apply relative
  my-5;
}

.dev {
  @apply p-10;
}

.icon {
  @apply absolute;
}

.icon img {
  @apply w-10;
}

.js_icon {
  @apply top-0
  right-1/4;
  animation: flip 3s linear infinite 2s;
}

.vue_icon {
  @apply top-10
  left-10;
  animation: flip 3s linear infinite;
}

.nuxt_icon {
  @apply bottom-0
  left-10;
  animation: flip 3s linear infinite 2s;
}

.css_icon {
  @apply top-1/4
  right-4;
  animation: flip 3s linear infinite ;
}

@keyframes flip {
  0% {
    transform: rotateY(0deg);
  }
  10% {
    transform: rotateY(90deg);
  }

  50% {
    transform: rotateY(0deg);
  }

  60% {
    transform: rotateY(-90deg);
  }

  100% {
    transform: rotateY(0deg);
  }
}

@keyframes wiggle {
  0% { transform: translate(1px, 1px) rotate(0deg); }
  10% { transform: translate(-1px, -2px) rotate(-1deg); }
  20% { transform: translate(-3px, 0px) rotate(1deg); }
  30% { transform: translate(5px, 4px) rotate(0deg); }
  40% { transform: translate(1px, -1px) rotate(1deg); }
  50% { transform: translate(-1px, 2px) rotate(-1deg); }
  60% { transform: translate(-3px, 1px) rotate(0deg); }
  70% { transform: translate(3px, 1px) rotate(-1deg); }
  80% { transform: translate(-1px, -1px) rotate(1deg); }
  90% { transform: translate(1px, 2px) rotate(0deg); }
  100% { transform: translate(1px, -2px) rotate(-1deg); }
}
</style>