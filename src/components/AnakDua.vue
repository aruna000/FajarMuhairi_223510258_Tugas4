<template>
  <div>
    <button @click="kirimdata">
      <img
        src="./rise.jpg"
        alt="Gambar Anak Satu"
        class="thumbnail"
      /><br />Rise
    </button>
  </div>
</template>

<script>
export default {
  methods: {
    kirimdata() {
      const dataLagu = {
        judul: "Rise - Jonas Blue feat. Jack & Jack",
        penyanyi: "Jonas Blue feat. Jack & Jack",
        tahun: 2018,
        deskripsi:
          "Rise adalah lagu yang dinyanyikan oleh produser musik dan DJ Inggris, Jonas Blue, dengan vokal dari duo pop-rap Amerika, Jack & Jack. Lagu ini dirilis pada tahun 2018 dan menjadi hit musim panas. Rise menceritakan tentang semangat pantang menyerah dan optimisme, di mana liriknya menginspirasi pendengarnya untuk terus bangkit menghadapi tantangan hidup. Lagu ini mengajak untuk menikmati hidup, tetap positif, dan tidak membiarkan halangan atau rintangan menghalangi jalan menuju impian dan tujuan. Dengan melodi yang ceria dan energik, Rise berhasil menginspirasi banyak orang dengan pesan motivasionalnya.",
      };
      this.$emit("sendData", dataLagu);
    },
  },
};
</script>

<style scoped>
.thumbnail {
  width: 50px;
  height: 50px;
  border-radius: 5px;
  align-items: center;
}

.button {
  display: flex;
  padding: 10px 20px;
  font-size: 16px;
  align-items: center;
  background-color: #007bff;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.button:hover {
  background-color: #0056b3;
}
</style>
