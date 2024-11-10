<template>
  <div class="preloader">
    <div v-for="(data, index) of list" :key="'index-' + index">
      <p v-if="index === showing" class="fs-1 text-body">
        {{ data }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      list: ["Hai!", "Hello!", "Assalamualaikum", "Warahmatullahi", "Wabarakatuh", ], // Kata-kata baru yang akan ditampilkan
      show: 0, // Menyimpan index kata yang sedang ditampilkan
    };
  },

  computed: {
    // Menghitung kata yang sedang ditampilkan, mengubahnya setiap interval
    showing() {
      setTimeout(() => {
        if (this.show < this.list.length - 1) {
          this.show++; // Menambah index untuk menampilkan kata berikutnya
        }
      }, 400); // Setiap 400ms, tampilkan kata berikutnya

      return this.show; // Mengembalikan index kata yang sedang ditampilkan
    },
  },
};
</script>

<style scoped>
.preloader {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background: #212529; /* Gradien dari #0a0606 ke #5e2e2e dengan sudut 135 derajat */
}


.text-body {
  font-size: 2rem;
  font-weight: bold;
  color: #ffffff; /* Warna teks putih */
  text-align: center;
}
</style>
