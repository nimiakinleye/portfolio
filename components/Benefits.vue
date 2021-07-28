<template>
  <div>
    <div class="benefits">
      <div class="benefit" data-aos="flip-up">
        <div class="glass"></div>
        <div class="not_glass">
          <img src="~/assets/api.svg" alt="" />
          <h4 class="title">API Consumption</h4>
          <p class="caption">
            I have demonstrated efficiency in the use of APIs. Including REST
            APIs and GraphQl
          </p>
        </div>
      </div>
      <div class="benefit" data-aos="flip-up" data-aos-delay="200">
        <div class="glass"></div>
        <div class="not_glass">
          <img src="~/assets/pixel_perfect.svg" alt="" />
          <h4 class="title">Pixel perfect UI Conversion</h4>
          <p class="caption">
            Because I pay attention to details when developing user interfaces,
            I am able to create pixel-perfect user interfaces.
          </p>
        </div>
      </div>
      <div class="benefit" data-aos="flip-up" data-aos-delay="400">
        <div class="glass"></div>
        <div class="not_glass">
          <img src="~/assets/responsive.svg" alt="" />
          <h4 class="title">Responsive User Interface</h4>
          <p class="caption">
            When developing user interfaces, I am on the lookout for
            responsiveness. To accomplish this, I thoroughly test my work on all
            possible screens and make changes as needed to ensure that it is
            displayed correctly.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import aosMixin from '~/mixins/aos'
export default {
  mixins: [aosMixin],
}
</script>

<style scoped>
.benefits {
  @apply flex
  flex-col
  items-center
  justify-center
  my-10
  text-white
  md:flex-row;
}

.benefit {
  @apply w-64
  h-52
  m-5
  bg-gray-700
  p-4
  rounded-2xl
  relative;
  background: rgb(2, 0, 32);
  background: linear-gradient(
    30deg,
    rgba(2, 0, 32, 1) 0%,
    rgba(52, 61, 78, 1) 46%,
    rgba(3, 89, 107, 1) 100%
  );
}

.benefit .title {
  @apply font-semibold
  my-0.5;
}

.benefit .caption {
  font-size: 0.7rem;
  @apply font-thin
  pr-1;
}

.not_glass {
  @apply absolute;
}

.glass {
  @apply absolute
  bg-black
  h-full
  w-full
  top-0
  left-0
  bg-opacity-50
  rounded-2xl
  z-0;
  background: rgba(121, 128, 139, 0.35);
  box-shadow: 0 8px 32px 0 rgba(31, 38, 135, 0.37);
  backdrop-filter: blur(4px);
  -webkit-backdrop-filter: blur(4px);
  border-radius: 10px;
  border: 1px solid rgba(255, 255, 255, 0.18);
  transition: 500ms;
}

/* .not.glass:hover > .glass:hover, .glass:hover {
  background: none;
  box-shadow: none;
  backdrop-filter: none;
  -webkit-backdrop-filter: none;
  border-radius: none;
  border: none;
} */

.benefit:hover > * {
  background: none;
  box-shadow: none;
  backdrop-filter: none;
  -webkit-backdrop-filter: none;
  border-radius: none;
  border: none;
  -webkit-animation: wiggle 0.5s;
  animation: wiggle 0.5s;
}

@keyframes wiggle {
  0% { transform: translate(1px, 1px) rotate(0deg); }
  10% { transform: translate(-1px, -2px) rotate(-1deg); }
  20% { transform: translate(-3px, 0px) rotate(1deg); }
  30% { transform: translate(3px, 2px) rotate(0deg); }
  40% { transform: translate(1px, -1px) rotate(1deg); }
  50% { transform: translate(-1px, 2px) rotate(-1deg); }
  60% { transform: translate(-3px, 1px) rotate(0deg); }
  70% { transform: translate(3px, 1px) rotate(-1deg); }
  80% { transform: translate(-1px, -1px) rotate(1deg); }
  90% { transform: translate(1px, 2px) rotate(0deg); }
  100% { transform: translate(1px, -2px) rotate(-1deg); }
}
</style>