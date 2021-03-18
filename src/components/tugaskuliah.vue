//tugaskuliah.vue
<template>
  <table class="table">
  <thead class="thead-light">
    <tr> 
      <th scope="col">Nama Tugas</th>
      <th scope="col">Mata Kuliah</th>  
      <th scope="col">Deadline</th>
    </tr>
  </thead>
  <tbody>
    <tr> 
      <td>Membuat Web Sederhana</td>
      <td>HTML & CSS Dasar</td> 
      <td>30 Maret 2021</td> 
    </tr>
    <tr> 
      <td>Struktur Data</td>
      <td>Struktur Data</td> 
      <td>20 Maret 2021</td> 
    </tr>
    <tr> 
      <td>Membuat Vue.JS</td>
      <td>Membuat Web tingkat lanjut</td> 
      <td>25 Maret 2021</td> 
    </tr> 
  </tbody>
  <tr v-for="tugaskuliah in tugaskuliah" :key="tugaskuliah.id">
  <template v-if="tugaskuliahId === customer.id">
    <td>
      <label for="name" class="font-weight-bold">Nama Tugas:</label>
      <div> 
        <input type="text" v-model="customer.name" class="form-control" />
      </div>
    </td>
    <td>
      <label for="email" class="font-weight-bold">Mata Kuliah:</label>
      <div> 
        <input type="text" v-model="customer.email" class="form-control" />
      </div>
    </td>
    <td>
      <label for="address" class="font-weight-bold">Deadline:</label>
      <div> 
        <input type="text" v-model="customer.address" class="form-control"  />
      </div>
    </td>
    <td>
      <button class="btn btn-success m-2" @click="saveEdit(tugaskuliah)">Save</button>
      <button class="btn btn-danger" @click="cancelEdit(tugaskuliah)" >Cancel</button>
    </td>
  </template>
  <template v-else>
    <td>{{customer.name}}</td>
    <td>{{customer.email}}</td>
    <td>{{customer.address}}</td>
    <td>
      <button class="btn btn-primary" @click="editCustomer(tugaskuliah)">Edit</button> 
    </td>
 </template>
</tr>
  <tbody>
  <tr v-for="tugaskuliah in tugaskuliah" :key="tugaskuliah.id"> 
    <td>{{ tugaskuliah.namatugas }}</td>
    <td>{{ tugaskuliah.matakuliah }}</td>
    <td>{{ tugaskuliah.deadline }}</td>
  </tr>  
</tbody>
</table>
</template>

<script>
  export default {
    name: 'tugaskuliah-table',
    props: {
      tugaskuliah: Array,
    },
  }
</script>

<style scoped>

</style>