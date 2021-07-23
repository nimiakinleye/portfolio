<template>
  <header>
    <div class="logo">
      <img src="~/assets/logo.png" alt="" />
    </div>
  </header>
</template>

<script>
export default {
  
}
</script>

<style scoped>
header {
  @apply bg-gray-800
  h-14;
}

.logo img {
  position: relative;
  top: 1rem;
  clear: both;
  @apply w-20
  mx-auto
  bg-gray-800
  rounded-full
  p-2;
}
</style>