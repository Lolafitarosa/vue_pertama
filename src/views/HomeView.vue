<template>
  <div class="home-page">
    <h1>Selamat Datang di Halaman Penjualan Es Krim</h1>
    <p>Nikmati kelezatan es krim kami yang segar dan lezat untuk memuaskan selera Anda.</p>
    
    <div class="feature-section">
      <h2>Pilihan Utama</h2>
      <ul>
        <li>Rasa Es Krim: Temukan berbagai pilihan rasa es krim premium kami.</li>
        <li>Paket Es Krim: Lihat paket-paket spesial untuk acara atau untuk menikmati bersama keluarga.</li>
        <li>Promosi: Jangan lewatkan penawaran spesial dan diskon terbaru hanya untuk Anda.</li>
      </ul>
    </div>
    
    <div class="call-to-action">
      <div class="cta-content">
        <p>Ingin mencoba es krim kami? Ayo pesan sekarang!</p>
        <button @click="redirectToAbout">Tentang Kami</button>
      </div>
      <img src="@/assets/logo.jpeg" alt="Ice Cream" class="ice-cream-photo">
    </div>
  </div>
</template>

<script setup>
import { useRouter } from 'vue-router';

const router = useRouter();

const redirectToAbout = () => {
  router.push('/about'); // Ganti dengan rute yang sesuai untuk halaman "About"
}
</script>

<style scoped>
/* Menggunakan font dari Google Fonts */
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600&display=swap');

.home-page {
  max-width: 900px;
  margin: 0 auto;
  padding: 20px;
  text-align: center;
  font-family: 'Montserrat', sans-serif; /* Menggunakan font Montserrat */
  color: #333; /* Warna teks utama */
  background-color: #fff; /* Latar belakang putih untuk kesan bersih */
  border-radius: 10px; /* Sedikit lengkungan pada tepi */
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1); /* Efek bayangan */
}

/* Judul */
.home-page h1 {
  font-size: 2.5rem;
  color: #3b012b; /* Warna teks judul yang cerah dan menarik */
  margin-bottom: 20px;
  font-weight: 600; /* Berat font yang lebih tebal untuk judul */
}

/* Paragraf */
.home-page p {
  font-size: 1.2rem;
  line-height: 1.8;
  color: #555; /* Warna teks yang lebih lembut */
  margin-bottom: 30px;
}

/* Bagian fitur */
.feature-section {
  margin-top: 30px;
  padding: 20px;
  background-color: #f0f8ff; /* Warna latar belakang lembut */
  border-radius: 10px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}

.feature-section ul {
  list-style-type: none;
  padding: 0;
  text-align: left; /* Teks dalam daftar di-align ke kiri */
}

.feature-section li {
  margin-bottom: 15px;
  font-size: 1rem;
  color: #333; /* Warna teks */
  transition: color 0.3s ease; /* Animasi pada perubahan warna teks */
}

.feature-section li:hover {
  color: #520039; /* Warna teks saat di-hover */
}

/* Bagian call-to-action */
.call-to-action {
  display: flex;
  align-items: center;
  justify-content: space-between; /* Menjaga jarak antara konten dan gambar */
  margin-top: 40px;
  padding: 20px; /* Memberikan sedikit padding untuk estetika */
  background-color: #fff7f7; /* Latar belakang lembut untuk kontras */
  border: 1px solid #ddd; /* Memberikan batas untuk memisahkan bagian */
  border-radius: 10px; /* Membulatkan sudut-sudutnya */
  box-shadow: 0 4px 10px rgba(231, 124, 255, 0.1);
}

.cta-content {
  max-width: 60%; /* Batasan lebar konten agar seimbang dengan gambar */
  text-align: left; /* Menyejajarkan teks ke kiri */
}

.ice-cream-photo {
  width: 150px; /* Ukuran gambar disesuaikan agar tidak terlalu besar */
  height: 150px; /* Menjaga aspek ratio dengan tinggi otomatis */
  margin-left: 20px; /* Ruang antara gambar dan teks */
  border-radius: 50%; /* Membulatkan gambar menjadi lingkaran */
  box-shadow: 0 4px 10px rgba(255, 127, 251, 0.2); /* Shadow pada gambar */
  transition: transform 0.3s ease, box-shadow 0.3s ease; /* Animasi pada transformasi dan shadow */
}

.ice-cream-photo:hover {
  transform: scale(1.1); /* Efek zoom saat di-hover */
  box-shadow: 0 8px 16px rgba(236, 127, 222, 0.3); /* Shadow lebih besar saat di-hover */
}

/* Tombol */
.call-to-action button {
  margin-top: 20px;
  padding: 14px 30px;
  font-size: 1.1rem;
  background-color: #5c033a;
  color: white;
  border: none;
  border-radius: 10px;
  cursor: pointer;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2); /* Shadow pada tombol */
  transition: background-color 0.3s, transform 0.3s, box-shadow 0.3s; /* Animasi pada background-color, transform, dan shadow */
}

.call-to-action button:hover {
  background-color: #510636;
  transform: translateY(-3px); /* Efek angkat saat di-hover */
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.3); /* Shadow lebih besar saat di-hover */
}
</style>
