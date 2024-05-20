<template>
  <div class="container">
    <h1 class="title">Kapsul Musik</h1>
    <h2 class="subtitle">Lagu Teratas</h2>
    <AnakSatu @sendData="receiveData" />
    <hr class="divider" />
    <AnakDua @sendData="receiveData" />
    <SlotComponent v-if="dataanak">
      <hr />
      <p><strong>Penyanyi:</strong> {{ dataanak.penyanyi }}</p>
      <p><strong>Tahun Keluaran:</strong> {{ dataanak.tahun }}</p>
      <p><strong>Deskripsi Lagu:</strong></p>
      <p>{{ dataanak.deskripsi }}</p>
      <p>{{ dataanak.imagePath }}</p>
    </SlotComponent>
  </div>
</template>

<script>
import AnakSatu from "./AnakSatu.vue";
import AnakDua from "./AnakDua.vue";
import SlotComponent from "./SlotComponent.vue";

export default {
  components: {
    AnakSatu,
    AnakDua,
    SlotComponent,
  },
  data() {
    return {
      dataanak: "",
    };
  },
  methods: {
    receiveData(data) {
      this.dataanak = data;
    },
  },
};
</script>

<style scoped>
.container {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
}

.title {
  text-align: center;
  font-size: 32px;
  color: #333;
  margin-bottom: 20px;
}

.subtitle {
  font-size: 24px;
  color: #666;
  margin-bottom: 10px;
}

.divider {
  border-top: 2px solid #ccc;
  margin: 20px 0;
}
</style>
