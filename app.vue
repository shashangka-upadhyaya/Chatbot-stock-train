<template>
  <!-- fresh started again  -->

  <div
    class="bg-repeat bg-cover w-full h-full font-sans"
    style="background-image: url(/bg.png)"
  >
    <!-- full video background code started  -->
    <video
      class="absolute top-0 left-0 w-full h-full object-cover"
      src="/matrix.mp4"
      loop
      autoplay
      muted
    ></video>

    <!-- full video background code ended  -->

    <div class="flex items-center justify-center h-full">
      <div
        class="max-w-[800px] relative z-20 shadow-lg after:content-[' '] after:z-[-1] after:h-full after:bg-slate-100 after:border after:border-slate-200 after:absolute after:left-2.5 after:right-2.5 after:top-0 after:mt-2 after:rounded"
      >
        <div class="bg-white border border-slate-200 p-6 rounded">
          <!-- Start Screen -->
          <Start v-if="!isChatting" />
          <!-- Chat Screen -->
          <Chat v-else />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const isChatting = useIsChatting();
</script>

<style>
html,
body,
#__nuxt {
  width: 100%;
  height: 100%;
}
</style>
