<template>
  <div class="tugaskuliah-form">
    <form>
      <div class="form-group">
        <label for="name">Nama Tugas</label>
        <input type="text" class="form-control" placeholder="Masukan nama pelanggan">
      </div>
      <div class="form-group">
        <label for="email">Mata Kuliah</label>
        <input type="text" class="form-control" placeholder="Masukan email pelanggan">
      </div>
      <div class="form-group">
        <label for="address">Deadline</label>
        <textarea type="text" class="form-control" 
          placeholder="Masukan alamat pelanggan"> </textarea>
      </div>
      <button type="submit" class="btn btn-primary">Submit</button>
    </form>
  </div>
</template>

<script>
  export default {
    name: 'tugaskuliah-form',
    data(){
      return {
        tugaskuliah: {
          namatugas: '',
          matakuliah: '',
          deadline: '',
        }
      }
    }
  }
</script>
