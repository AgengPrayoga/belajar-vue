<script setup>
let mgs = "Hallo Dunia";
let headName = "<h1>Nama Saya Ageng</h1>"
let number = 7;
let ok = "NO";
let seen = true

// pengulangan
let todos = [
  { teks: 'Belajar JavaScript'},
  { teks: 'Belajar Vue'},
  { teks: 'Buat Proyek keren'}
]

// Input
let pesan = ref("Hai Vue");
</script>
<template>
  <div>
    <span> {{ mgs }} </span> <br>
    <span style="color: red;">Ini Warna Merah</span> <br>
    <span v-html="headName"></span> <br>
     <a href="https://youtube.com/"><button v-bind:link="Dynamiclink" >Tombol</button></a> <br>
    
  </div>
  <p>{{ message }}</p>
  <button v-on:click="balikkanPesan">Balikkan Pesan</button>

  <br> pengulangan
  <ol>
    <li v-for="todo in todos">
    {{ todo.teks }}</li>
  </ol>

  <p>{{ pesan }}</p>
  <input v-model="pesan">
</template>