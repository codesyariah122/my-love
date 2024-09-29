<template>
  <section class="relative h-screen">
    <!-- Background Video -->
    <div class="absolute inset-0 z-0 overflow-hidden">
   
      <iframe
        class="w-full h-full"
        src="https://www.youtube.com/embed/2HzcTCUqAEw?si=JTSE0g-3KxO-xfpU&autoplay=1&mute=1&loop=1&playlist=2HzcTCUqAEw&controls=0&showinfo=0&modestbranding=0&rel=0"
        title="YouTube video player"
        frameborder="0"
        allow="accelerometer; fullscreen; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
        referrerpolicy="strict-origin-when-cross-origin"
        allowfullscreen
      ></iframe>
    </div>

    <!-- Content on top of the video -->
    <div
      class="relative z-10 flex items-center justify-center h-full bg-black bg-opacity-50"
    >
      <div class="text-center text-white">
        <h1 class="text-5xl font-extrabold mb-4">Welcome to Our Love Story</h1>
        <p class="text-xl">The Journey of Puji Ermanto & Fitri Kulsum</p>
        <a
          href="#about"
          class="mt-6 inline-block px-8 py-3 bg-pink-600 hover:bg-pink-700 rounded-full text-lg font-bold"
        >
          Learn More
        </a>
      </div>
    </div>
  </section>
</template>

<script setup>
// You can customize the video by changing the YouTube video URL in the iframe src
</script>

<style scoped>
/* Optional: add some custom styles here */
</style>
