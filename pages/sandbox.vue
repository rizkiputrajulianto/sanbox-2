<template>
  <div>
    <h1>Sandbox Frontend 1</h1>
    <div class="row">
      <!-- judul -->
      <div class="col-sm-4">
        <input
          type="text"
          class="border border-info rounded-pill"
          v-model="vale"
          id="judulInput"
        />
        <button
          @click="tambahJudul"
          type="button"
          class="btn btn-outline-info rounded-pill"
        >
          Tambahkan
        </button>
        <div v-for="(item, i) in judulBuku" :key="i">
          <items-judul :judul="item" @del="deletedata" />
        </div>
      </div>
      <!-- nama -->
      <div class="col-sm-4">
        <input type="text" class="border border-info rounded-pill" />
        <button
          @click="tambahNama"
          type="button"
          class="btn btn-outline-info rounded-pill"
        >
          Tambahkan
        </button>
        <items-nama />
      </div>
      <!-- gabungan -->
      <div class="col-sm-4">
        <div class="input-group mb-3">
          <select class="custom-select" id="inputGroupSelect02">
            <option selected>Choose...</option>
            <option value="1">One</option>
            <option value="2">Two</option>
            <option value="3">Three</option>
          </select>
          <select class="custom-select" id="inputGroupSelect02">
            <option selected>Choose...</option>
            <option value="1">One</option>
            <option value="2">Two</option>
            <option value="3">Three</option>
          </select>
        </div>

        <button
          @click="tambahGabungan"
          type="button"
          class="btn btn-outline-info rounded-pill"
        >
          Tambahkan
        </button>
        <items-gabungan />
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      val: "",
      judulBuku: ["Bahasa Inggris", "Bahasa Indonesia"],
    };
  },
  computed: {
    vale: {
      set(value) {
        const [first, ...second] = value.split(" ");
        this.val = first.concat(second);
      },
    },
  },
  methods: {
    tambahJudul() {
      const data = this.val;
      this.judulBuku.push(data);
    },
    deletedata(data) {
      this.judulBuku.remove(data);
    },
  },
};
</script>