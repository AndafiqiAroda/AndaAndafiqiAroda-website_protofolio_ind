<script>
export default {
  data(){return{
    educations: [
    {
        year: "2019 - 2021",
        univ: "SMA Negeri 2",
        location: "Sorong, Papua Barat",
        degree: "Sekolah Menengah Atas (SMA)",
        field: "Ilmu Pengetahuan Alam (IPA)",
        description: [
          "Pada jurusan IPA, saya belajar banyak hal. Mulai dari ilmu matematika, ilmu alam, dan juga ilmu komputer sesekali.",
          "Saya lulus dengan keterangan sangat baik.",
        ]
      },
      {
        year: "2021 - Sekarang",
        univ: "Universitas Amikom Yogyakarta",
        location: "Yogyakarta",
        degree: "Sarjana (S1)",
        field: "Informatika",
        description: [
          "Dalam bidang study informatika, saya mempelajari banyak hal tentang basic - basic Web Development, Design Website, Photography, Data Mining, dan juga Machine learning. ",
          "Saya pun tetap mempelajari banyak hal mengenai pengembangan teknologi sampai dengan saat ini.",
        ]
      },
    ]
  }}
}
</script>

<template>
  <section>
    <h2 class="text-gradient fw-bolder mb-4">Pendidikan</h2>

    <div v-for="education of educations" class="card shadow border-0 rounded-4 mb-5">
      <div class="card-body px-3 px-md-5 py-5">
        <div class="row align-items-center gx-5">
          <div class="col text-center text-lg-start mb-4 mb-lg-0">
            <div class="p-4 rounded-4">
              <div class="text-gradient fw-bolder mb-2">{{education.year}}</div>
              <div class="mb-2">
                <div class="small fw-bolder">{{education.univ}}</div>
                <div class="small text-muted">{{education.location}}</div>
              </div>
              <div class="fst-italic">
                <div class="small text-muted">{{education.degree}}</div>
                <div class="small text-muted">{{education.field}}</div>
              </div>
            </div>
          </div>
          <div class="col-lg-8">
            <div>
              <ul class="mb-0">
                <li v-for="desc of education.description">
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