<template>
  <div class="about-page">
    <h1>Tentang Kami</h1>
    <p>Kami adalah penyedia es krim premium yang berkomitmen untuk menyajikan produk berkualitas tinggi untuk Anda. Setiap es krim kami dibuat dengan bahan-bahan terbaik dan rasa yang lezat.</p>

    <div class="ice-cream-gallery">
      <img src="@/assets/icecream-delivery.jpeg" alt="Ice Cream Delivery" class="feature-image">
      <img src="@/assets/wedding-icecream.jpeg" alt="Wedding Ice Cream" class="feature-image">
      <img src="@/assets/icecream-flavors.jpeg" alt="Variety of Ice Cream Flavors" class="feature-image">
    </div>

    <router-link to="/beranda" class="btn">pesan</router-link>
  </div>
</template>

<script setup>
// Tidak ada skrip untuk halaman ini saat ini
</script>

<style scoped>
/* Menggunakan font dari Google Fonts untuk estetika yang lebih baik */
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600&display=swap');

/* Style utama untuk halaman about */
.about-page {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
  text-align: center;
  margin-top: 50px;
  font-family: 'Montserrat', sans-serif; /* Menggunakan font Montserrat */
  color: #333; /* Warna teks utama */
  background-color: #f9f9f9; /* Latar belakang lembut */
  border-radius: 10px; /* Sedikit lengkungan pada tepi */
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1); /* Efek bayangan */
  padding: 30px; /* Padding lebih untuk ruang konten */
}

/* Judul */
.about-page h1 {
  font-size: 2.5rem;
  color: #6c0143; /* Warna judul yang lebih dalam */
  margin-bottom: 20px;
  font-weight: 600; /* Berat font yang lebih tebal untuk judul */
}

/* Paragraf */
.about-page p {
  font-size: 1.2rem;
  line-height: 1.8;
  color: #555; /* Warna teks yang lebih lembut */
  margin-bottom: 30px;
}

/* Galeri gambar */
.ice-cream-gallery {
  margin-top: 50px;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 40px;
}

/* Gambar dalam galeri */
.feature-image {
  max-width: 100%;
  height: auto;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Efek shadow */
  transition: transform 0.3s ease, box-shadow 0.3s ease, border 0.3s ease; /* Animasi pada transformasi, shadow, dan border */
}

.feature-image:hover {
  transform: scale(1.05); /* Efek zoom saat di-hover */
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2); /* Shadow lebih besar saat di-hover */
  border: 2px solid #ac4caf; /* Border yang stylish saat di-hover */
}

/* Tombol */
.btn {
  margin-top: 40px;
  padding: 14px 50px; /* Memperpanjang tombol dan memberikan lebih banyak padding */
  font-size: 16px;
  background-color: #6f0072;
  color: white;
  border: none;
  border-radius: 10px; /* Border radius lebih besar untuk efek yang lebih lembut */
  cursor: pointer;
  text-decoration: none;
  display: inline-block;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); /* Shadow pada tombol */
  transition: background-color 0.3s, transform 0.3s, box-shadow 0.3s; /* Animasi pada background-color, transform, dan shadow */
}

.btn:hover {
  background-color: #6c0143; /* Warna saat di-hover */
  transform: translateY(-3px); /* Efek angkat saat di-hover */
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.3); /* Shadow lebih besar saat di-hover */
}
</style>
