//App.vue
<template>
  <div id="app">
    <div class="container">
      <h1 class="mb-4">Tugas Kuliah</h1>
       <hr>
      <p> 
        <button class="btn btn-primary" type="button" data-toggle="collapse" data-target="#collapseExample" aria-expanded="false" aria-controls="collapseExample">
        Tambah Tugas
        </button>
      </p> 
      <tugaskuliah-table v-bind:tugaskuliah='tugaskuliah'/>

      <div class="collapse" id="collapseExample">
        <div class="card card-body">
          <h2>Input Tugas Kuliah</h2>
          <hr>

      <tugaskuliah-table />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import tugaskuliah from '@/components/tugaskuliah.vue'
import tugaskuliahform from '@/components/tugaskuliahform.vue'

export default {
  name: 'App',
  Components: {
    tugaskuliah,
    tugaskuliahform,
  },
  data() {
    return {
      tugaskuliah: [
        {
          id: 1,
          namatugas: 'Membuat Web Sederhana',
          matakuliah: 'HTML & CSS Dasar',
          deadline: '30 Maret 2021',
        },
        {
          id: 2,
          namatugas: 'Struktur Data',
          matakuliah: 'Struktur Data',
          deadline: '20 Maret 2021',
        },
        {
          id: 3,
          namatugas: 'Membuat Vue.JS',
          matakuliah: 'Membuat Web tingkat lanjut',
          deadline: '25 Maret 2021',
        },
      ],
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  margin-top: 60px;
}
</style>