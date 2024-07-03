<template>
  <div id="app">
    <nav>
      <a href="/">Home</a>
      <a href="/about">About</a>
      <a href="/beranda">Beranda</a>
    </nav>

    <router-view />

    <footer>
      <p>&copy; 2024 Ice Cream Shop</p>
    </footer>
  </div>
</template>

<script setup>
// Tidak ada yang perlu diubah dalam setup script jika Anda tidak menggunakan router
</script>

<style>
/* Gaya untuk navigasi dan elemen utama di luar blok scoped */
#app {
  max-width: 600px;
  margin: 0 auto;
  padding: 20px;
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: center; /* Memusatkan vertikal */
  align-items: center; /* Memusatkan horizontal */
  min-height: 100vh; /* Menyertakan ketinggian minimum seluruh viewport */
}


nav {
  background-color: #f0f0f0;
  padding: 10px 0;
  margin-bottom: 20px;
  display: flex;
  justify-content: center;
  width: 100%;
}

nav a {
  text-decoration: none;
  color: #555;
  padding: 5px;
  margin: 0 5px;
  border-radius: 2px;
  transition: background-color 0.3s ease;
}

nav a:hover {
  background-color: #ddd;
}

footer {
  border-top: 1px solid #ccc;
  color: #888;
}
</style>
