<template>
  <div class="slot-container">
    <h1>Detail Lebih Lanjut</h1>
    <div class="slot-content">
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "SlotComponent",
};
</script>

<style scoped>
.slot-container {
  border: 2px solid #ccc;
  border-radius: 8px;
  padding: 20px;
}

.slot-content {
  margin-top: 10px;
}

.slot-content p {
  margin-bottom: 10px;
  line-height: 1.5;
}

.slot-content strong {
  color: #007bff;
}

.slot-content em {
  font-family: "Trebuchet MS", sans-serif;
}
</style>
