<template>
  <div>
    <div class="row my-3">
      <div class="col-sm-8">
        <p>{{ judul }}</p>
      </div>
      <div class="col-sm-4">
        <button
          class="btn btn-outline-info"
          style="text-size: 20px"
          @click="hapus"
        >
          Delete
        </button>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    judul: { type: String, default: "" },
  },
  methods: {
    hapus() {
      const data = this.judul;
      this.$emit("del", data);
    },
  },
};
</script>