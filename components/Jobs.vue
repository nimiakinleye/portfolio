<template>
  <div class="my-10 w-10/12 mx-auto lg:ml-auto">
    <div class="flex flex-col shadow-2xl">
      <img class="rounded-t-lg" src="~/assets/cashdrive.png" alt="" />
      <div class="flex justify-between my-bg py-4 p-2 rounded-b-lg">
        <a href="#">https://cashdrive.co/</a>
        <svg
          width="24"
          height="24"
          viewBox="0 0 24 24"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M21 3L13.93 19.97L11.42 12.58L4.03 10.07L21 3Z"
            stroke="white"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
          />
          <path
            d="M11 13L5 19"
            stroke="white"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
          />
        </svg>
      </div>
    </div>
    <h4 class="firm">Cashdrive</h4>
    <p class="job_description">
      Solely responsible for the development of the product’s app user
      intercace, ranging from the User App to the Admin App. The afore mentioned
      was achieved with NuxtJs, an extended framework of VueJs which is a
      framework of JavaScript.
    </p>
  </div>
</template>

<script>
import aosMixin from '~/mixins/aos'
export default {
  mixins: [aosMixin]
}
</script>

<style>
.my-bg {
  background-color: #374151;
}

a {
  color: white;
}

.firm {
  @apply font-bold
  my-1;
  color: #374151;
}

.job_description {
  @apply text-sm
}
</style>