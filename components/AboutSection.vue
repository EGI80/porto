<template>
  <section class="about" id="about">
    <div class="container">
      <h2>About Me</h2>
      <div class="about-content">
          <div class="about-text" ref="aboutText">
            <p>Nama: EGI
           </p>
            <p>Studi: Universitas AMIKOMI</p>
            <p>Domisili: Yogyakarta</p>
            <p>Saya adalah seorang mahasiswa aktif di Universitas AMIKOM di Yogyakarta, fokus pada pengembangan teknologi </p> <p>informasi. Saya memiliki keahlian dalam pengembangan web secara fullstack, yang meliputi baik frontend</p>
              <p> maupun backend. Dengan pengalaman dalam menggunakan teknologi seperti React untuk pengembangan frontend,</p>
                <p>serta PHP dan Laravel untuk pengembangan backend, saya berusaha untuk mengintegrasikan kedua sisi ini</p>
                <p> dengan baik dalam proyek-proyek saya</p>
                  <p></p>
        </div>
        <img src="https://bootdey.com/img/Content/avatar/avatar7.png" alt="Profile Picture" class="about-image"/>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'AboutSection',
  mounted() {
    // Jalankan animasi masuk setelah komponen dimuat
    this.animateIn();
  },
  methods: {
    animateIn() {
      // Tambahkan class untuk animasi pada div about-text setelah komponen dimuat
      this.$refs.aboutText.classList.add('fade-in');
    }
  }
}
</script>

<style scoped>
.about {
  padding: 50px 0;
  background: linear-gradient(90deg, rgba(0, 0, 50, 0.9), rgba(0, 0, 100, 0.9));
  border-bottom: 2px solid #dc3545;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

h2 {
  text-align: center;
  margin-bottom: 40px;
  font-size: 2.5em;
  color: #00FFEE;
  text-shadow: 0 0 10px #00FFEE, 0 0 20px #00FFEE;
}

.about-content {
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 40px; /* Tambahkan jarak antara gambar dan teks */
  padding: 20px; /* Tambahkan padding untuk memberikan ruang sekitar */
}

.about-image {
  width: 250px; /* Perbesar gambar */
  height: 250px;
  border-radius: 50%;
  object-fit: cover;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Tambahkan bayangan untuk efek modern */
  transition: transform 0.3s ease; /* Animasi transformasi */
}

.about-image:hover {
  transform: scale(1.1); /* Perbesar gambar saat di-hover */
}

.about-text {
  max-width: 800px;
  text-align: left;
  color: #FFF;
  opacity: 0; /* Awalnya atur opacity menjadi 0 */
}

.about-text p {
  margin-bottom: 20px;
  line-height: 1.6;
  overflow: hidden; /* Sembunyikan overflow teks */
  white-space: nowrap; /* Teks tidak pindah ke baris baru */
  animation: typing 4s steps(40, end) forwards; /* Animasi ketik */
}

@keyframes typing {
  from { width: 0 }
  to { width: 100% }
}

/* Animasi untuk fade-in */
.fade-in {
  opacity: 1;
  transition: opacity 1s ease;
}
</style>
