<template>
<div>
  <header class="relative flex items-center justify-center h-screen overflow-hidden">
    <video autoplay loop muted playsinline class="fixed z-10 w-full ">
      <source src="/bg.mp4" type="video/mp4" />
    </video>
    <video autoplay loop muted playsinline class="fixed z-10 w-full min-[500px]:hidden">
      <source src="/bgm.mp4" type="video/mp4" />
    </video>


  </header>

</div>
</template>

<script>
export default {
name:'home'
}
</script>

<style>

</style>
