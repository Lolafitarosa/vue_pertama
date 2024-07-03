<template>
  <div class="container">
    <div class="header">
      <div class="overlay">
        <h1>{{ title }}</h1>
      </div>
      <img src="@/assets/logo.jpeg" alt="Ice Cream" class="ice-cream-photo">
    </div>
    <br>
    <h2>Total Penjualan: <span class="result">{{ result }}</span></h2>

    <div class="form-group">
      <label for="jumlahEsKrim">Jumlah Es Krim</label>
      <input type="number" id="jumlahEsKrim" v-model="jumlahEsKrim" class="form-control" placeholder="Masukkan jumlah es krim" />
    </div>
    <div class="form-group">
      <label for="hargaPerEsKrim">Harga per Es Krim</label>
      <input type="number" id="hargaPerEsKrim" v-model="hargaPerEsKrim" class="form-control" placeholder="Masukkan harga per es krim" />
    </div>
    <button @click="calculateTotal" class="btn">Hitung Total Penjualan</button>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const title = ref('Kalkulator Penjualan Es Krim')
const result = ref('')
const jumlahEsKrim = ref('')
const hargaPerEsKrim = ref('')

const calculateTotal = () => {
  const jumlah = parseFloat(jumlahEsKrim.value)
  const harga = parseFloat(hargaPerEsKrim.value)
  
  if (!isNaN(jumlah) && !isNaN(harga)) {
    result.value = `Rp ${ (jumlah * harga).toFixed(2) }`
  } else {
    result.value = "Masukkan jumlah dan harga yang valid"
  }
}
</script>

<style scoped>
/* Menggunakan font dari Google Fonts */
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600&display=swap');

.container {
  max-width: 400px;
  margin: 0 auto;
  padding: 30px;
  text-align: center;
  background-color: #fafafa; /* Latar belakang abu-abu muda */
  border-radius: 12px;
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.1);
  font-family: 'Montserrat', sans-serif;
  color: #444;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
}

.header {
  position: relative;
  margin-bottom: 20px;
}

.overlay {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background-color: rgba(255, 255, 255, 0.8); /* Warna latar belakang semi-transparan */
  padding: 10px 20px;
  border-radius: 8px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1); /* Efek bayangan untuk kejelasan */
}

.overlay h1 {
  font-size: 2rem;
  color: #333; /* Warna judul lebih gelap */
}

.ice-cream-photo {
  width: 80px;
  height: 80px;
  border-radius: 50%;
}

h2 {
  font-size: 1.6rem;
  margin-bottom: 20px;
  color: #666; /* Warna subtitle abu-abu lebih gelap */
}

.result {
  font-weight: bold;
  color: #560054; /* Warna yang sama dengan tombol untuk konsistensi */
}

.result::before {
  content: "Rp ";
}

.form-group {
  margin-bottom: 20px;
  width: 100%;
  text-align: left;
}

label {
  font-weight: bold;
  display: block;
  margin-bottom: 8px;
  color: #888; /* Warna label abu-abu lebih terang */
}

input {
  padding: 12px;
  width: calc(100% - 24px);
  border: 1px solid #ddd;
  border-radius: 8px;
  font-size: 16px;
  background-color: #f5f5f5; /* Warna input abu-abu muda */
  box-shadow: inset 0 1px 3px rgba(0, 0, 0, 0.1);
  transition: border-color 0.3s; /* Animasi perubahan warna border saat fokus */
}

input:focus {
  border-color: #560054; /* Warna border saat input difokuskan */
}

button {
  padding: 14px 35px;
  font-size: 18px;
  background-color: #560054;
  color: white;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  transition: background-color 0.3s, transform 0.3s, box-shadow 0.3s;
}

button:hover {
  background-color: #4b0046;
  transform: translateY(-2px);
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
}
</style>
