<script>
export default {
  data(){
    return {
      experiences:[
        {
          year: "2023",
          jobs: "Data Scientist",
          company: "Google Colab",
          location: "Yogyakarta",
          description: [
            "Membuat sebuah machine learning yang dapat mendeteksi jenis barang dari foto yang kita kirimkan secara otomatis.",
          ]
        },
        {
          year: "2023",
          jobs: "UI/UX desainer",
          company: "Figma",
          location: "",
          description: [
            "Mendesain tampilan aplikasi Mbanking menggunakan figma dengan judul BB bank yang memiliki fitur spesial yaitu bisa langsung mendeteksi emoney dan juga rekening bank hanya dengan menggunakan nomer rekening ataupun virtual numbernya.",
          ]
        },
        {
          year: "2024",
          jobs: "Game Developer",
          company: "itch.io",
          location: "",
          description: [
            "Membuat game bertema spacewar bersama kelompok saya yang di upload di itch.io dengan judul bedil's Aircraft.",
          ]
        }
      ]
    }
  }
}
</script>

<template>
  <section>
    <div class="d-flex align-items-center justify-content-between mb-4">
      <h2 class="text-gradient fw-bolder mb-0">Pengalaman</h2>
<!--      <a class="btn btn-primary px-4 py-3" href="#!">-->
<!--        <div class="d-inline-block bi bi-download me-2"></div>-->
<!--        Download Resume-->
<!--      </a>-->
    </div>

    <div v-for="experience of experiences" :key="'experience-index-' + experience.company" class="card shadow border-0 rounded-4 mb-5">
      <div class="card-body px-3 px-md-5 py-5">
        <div class="row align-items-center gx-5">
          <div class="col text-center text-lg-start mb-4 mb-lg-0">
            <div class="p-4 rounded-4">
              <div class="text-gradient fw-bolder mb-2">{{experience.year}}</div>
              <div class="small fw-bolder">{{experience.jobs}}</div>
              <div class="small text-muted">{{experience.company}}</div>
              <div class="small text-muted">{{experience.location}}</div>
            </div>
          </div>
          <div class="col-lg-8">
            <div>
              <ul class="mb-0">
                <li v-for="desc of experience.description">
                  {{desc}}
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>

</style>