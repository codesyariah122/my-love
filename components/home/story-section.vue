<template>
  <section id="about" class="py-12 bg-gray-100">
    <div class="container mx-auto text-center">
      <h2 class="text-4xl font-bold mb-8">Pertemuan Pertama</h2>
      <!-- Swiper Slider Section -->
      <swiper
        ref="mySwiper"
        :slides-per-view="1"
        loop
        autoplay
        speed="800"
        space-between="20"
        grab-cursor="true"
        class="mySwiper"
      >
        <!-- Slide 1 - DM Instagram -->
        <swiper-slide>
          <div
            class="grid grid-cols-1 md:grid-cols-2 p-8 bg-white shadow-lg rounded-lg transform transition duration-500 hover:scale-105"
          >
            <!-- Deskripsi -->
            <div class="md:pr-8">
              <h3 class="text-2xl font-semibold mb-4">
                Komunikasi Berlanjut di WhatsApp
              </h3>
              <p class="text-lg mb-6">
                Setelah beberapa waktu berbicara melalui platform, kami merasa
                lebih nyaman untuk melanjutkan komunikasi ke WhatsApp. Di
                sinilah kami mulai berbagi cerita lebih dalam tentang mimpi dan
                harapan kami, semakin hari komunikasi kami semakin intens.
              </p>
            </div>
            <!-- Gambar -->
            <div class="flex justify-center">
              <img
                src="/assets/puji-fitri/IMG-20240820-WA0140.jpg"
                alt="Chat WhatsApp"
                class="rounded-lg w-80"
              />
            </div>
          </div>
        </swiper-slide>

        <!-- Slide 2 - Chat WhatsApp -->
        <swiper-slide>
          <div
            class="grid grid-cols-1 md:grid-cols-2 p-8 bg-white shadow-lg rounded-lg transform transition duration-500 hover:scale-105"
          >
            <!-- Deskripsi -->
            <div class="md:pr-8">
              <h3 class="text-2xl font-semibold mb-4">
                Komunikasi di WhatsApp
              </h3>
              <p class="text-lg mb-6">
                Setelah saling mengenal di Instagram, kami memutuskan untuk
                melanjutkan percakapan melalui WhatsApp. Dari sini, percakapan
                kami semakin intens dan mendalam, membicarakan banyak hal
                tentang mimpi dan harapan kami.
              </p>
            </div>
            <!-- Gambar -->
            <div class="flex justify-center">
              <img
                src="/assets/puji-fitri/IMG-20240922-WA0005.jpg"
                alt="Chat WhatsApp"
                class="rounded-lg w-80"
              />
            </div>
          </div>
        </swiper-slide>

        <!-- Slide 3 - Kunjungan ke Rumah -->
        <swiper-slide>
          <div
            class="grid grid-cols-1 md:grid-cols-2 p-8 bg-white shadow-lg rounded-lg transform transition duration-500 hover:scale-105"
          >
            <!-- Deskripsi -->
            <div class="md:pr-8">
              <h3 class="text-2xl font-semibold mb-4">
                Pertemuan Pertama di Rumah
              </h3>
              <p class="text-lg mb-6">
                Setelah berminggu-minggu berbicara melalui pesan, Puji akhirnya
                berkunjung ke rumah Fitri untuk pertama kalinya. Dengan penuh
                rasa gugup dan semangat, ia bertemu dengan Ayah dan Ibu Fitri
                dan resmi memulai hubungan mereka.
              </p>
            </div>
            <!-- Gambar -->
            <div class="flex justify-center">
              <img
                src="/assets/puji-fitri/IMG-20240826-WA0000.jpg"
                alt="Kunjungan Pertama"
                class="rounded-lg w-80"
              />
            </div>
          </div>
        </swiper-slide>

        <!-- Slide 4 - Kenangan Pertemuan -->
        <swiper-slide>
          <div
            class="grid grid-cols-1 md:grid-cols-2 p-8 bg-white shadow-lg rounded-lg transform transition duration-500 hover:scale-105"
          >
            <!-- Deskripsi -->
            <div class="md:pr-8">
              <h3 class="text-2xl font-semibold mb-4">Kenangan Pertemuan</h3>
              <p class="text-lg mb-6">
                Kunjungan pertama ini meninggalkan kesan yang mendalam bagi
                keduanya, dimana Puji dan Fitri merasa bahwa ini adalah awal
                dari perjalanan cinta yang akan mereka jalani bersama.
              </p>
            </div>
            <!-- Gambar -->
            <div class="flex justify-center">
              <img
                src="/assets/puji-fitri/Polish_20240817_143820698.jpg"
                alt="Kenangan Pertemuan"
                class="rounded-lg w-80"
              />
            </div>
          </div>
        </swiper-slide>
      </swiper>

      <div class="flex justify-center mt-4">
        <button @click="slideToPrev" class="swiper-button-prev">
          &#10094; Prev
        </button>
        <button @click="slideToNext" class="swiper-button-next">
          Next &#10095;
        </button>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, onMounted } from "vue";
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/swiper-bundle.css";
import "swiper/css/autoplay";
import "swiper/css/navigation";

const mySwiper = ref(null);

const slideToNext = () => { 
  if (mySwiper.value) {
    mySwiper.value.swiper.slideNext();
  }
};

const slideToPrev = () => {
  if (mySwiper.value) {
    mySwiper.value.swiper.slidePrev();
  }
};

onMounted(() => {
  if (mySwiper.value) {
    mySwiper.value.swiper.update();
    console.log(mySwiper.value.swiper); // Ensure swiper instance is accessible
  }
});
</script>

<style scoped>
.mySwiper {
  max-width: 700px;
  margin: 0 auto;
}

.swiper-slide {
  display: flex;
  justify-content: center;
  align-items: center;
  transition: all 0.3s ease;
}

.swiper-slide:hover {
  transform: scale(1.05);
}

.swiper-button-next,
.swiper-button-prev {
  position: absolute; /* Ubah posisi menjadi absolute */
  top: 150%; /* Posisi vertikal tengah */
  transform: translateY(-50%); /* Pusatkan tombol secara vertikal */
  z-index: 10; /* Pastikan tombol muncul di atas slide */
}

.swiper-button-prev {
  left: 10px; /* Sesuaikan jarak dari kiri */
}

.swiper-button-next {
  right: 10px; /* Sesuaikan jarak dari kanan */
}
</style>
