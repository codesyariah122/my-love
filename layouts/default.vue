<template>
  <div>
    <header class="bg-gray-800 text-white p-4">
      <nav class="container mx-auto flex justify-between items-center">
        <div class="text-lg font-bold">Puji & Fitri</div>
        <div class="hidden md:flex space-x-4">
          <ul class="flex space-x-4">
            <li><a href="/" class="hover:underline">Home</a></li>
            <li><a href="#about" class="hover:underline">About</a></li>
            <li><a href="#vision" class="hover:underline">Vision & Mission</a></li>
            <li><a href="#gallery" class="hover:underline">Gallery</a></li>
          </ul>
        </div>
        <div class="md:hidden">
          <button id="menu-button" class="focus:outline-none">
            <svg
              class="w-6 h-6"
              fill="none"
              stroke="currentColor"
              viewBox="0 0 24 24"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M4 6h16M4 12h16m-7 6h7"
              ></path>
            </svg>
          </button>
        </div>
      </nav>
      <div id="mobile-menu" class="md:hidden hidden">
        <ul class="flex flex-col space-y-2 p-4 bg-gray-700">
          <li><a href="/" class="hover:underline">Home</a></li>
          <li><a href="#about" class="hover:underline">About</a></li>
          <li><a href="#vision" class="hover:underline">Vision & Mission</a></li>
          <li><a href="#gallery" class="hover:underline">Gallery</a></li>
        </ul>
      </div>
    </header>

    <NuxtPage />

    <footer class="bg-gray-800 text-white p-4 mt-8">
      <div class="container mx-auto text-center">
        <p>&copy; 2024 Puji & Fitri's Love Journey</p>
      </div>
    </footer>
  </div>
</template>

<script setup>
import { onMounted } from 'vue';

onMounted(() => {
  const menuButton = document.getElementById("menu-button");
  const mobileMenu = document.getElementById("mobile-menu");

  menuButton.addEventListener("click", () => {
    mobileMenu.classList.toggle("hidden");
  });
});
</script>
