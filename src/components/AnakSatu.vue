<template>
  <div>
    <button @click="kirimdata">
      <img
        src="./mirrors.jpg"
        alt="Gambar Anak Satu"
        class="thumbnail"
      /><br />Mirros
    </button>
  </div>
</template>

<script>
export default {
  methods: {
    kirimdata() {
      const dataLagu = {
        judul: "Mirrors - Justin Timberlake",
        penyanyi: "Justin Timberlake",
        tahun: 2013,
        deskripsi:
          "Mirrors adalah lagu yang dirilis sebagai bagian dari album studio ketiga Justin Timberlake, The 20/20 Experience. Lagu ini menceritakan tentang refleksi diri dan hubungan yang mendalam antara dua orang yang saling mencintai. Liriknya menggambarkan bagaimana pasangan tersebut saling melengkapi dan menemukan bagian dari diri mereka dalam satu sama lain, seperti cermin yang mencerminkan perasaan dan pengalaman mereka. Lagu ini juga terinspirasi dari hubungan pribadi Timberlake, khususnya dedikasinya kepada istrinya, Jessica Biel, serta kakek-neneknya yang memiliki hubungan yang kuat dan bertahan lama.",
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
