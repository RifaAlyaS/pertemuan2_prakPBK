<template>
  <div>
    <input type="text" v-model="inputText" placeholder="Masukkan teks yang ingin diubah">
    <button @click="toggleColor">Ubah Warna</button>
    <div :class="{ 'purple': iniWarna }" :style="{ 'font-size': fontSize + 'px' }">
      {{ inputText }}
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputText: '', // Teks input yang dimasukkan oleh pengguna
      iniWarna: false,
      fontSize: 16
    };
  },
  methods: {
    toggleColor() {
      this.iniWarna = !this.iniWarna;
      this.fontSize += 2;
    }
  }
};
</script>

<style>
.purple{
  color: rgb(207, 0, 173);
}
</style>