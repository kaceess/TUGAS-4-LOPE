<!-- PinkChildComponent.vue -->
<template>
    <div class="child-component">
      <h3 style="color: #ff0066;">Child Component</h3>
      <button @click="sendDataToParent">Send Data to Parent</button>
    </div>
  </template>
  
  <script>
  export default {
    methods: {
      sendDataToParent() {
        this.$emit('childData', 'TEGAR HANIP BEST ASDOS EVERRR');
      }
    }
  };
  </script>
  
  <style scoped>
  .child-component {
    background-color: #ffcccc;
    padding: 10px;
    border-radius: 5px;
  }
  
  /* Menentukan warna teks untuk komponen anak */
  .child-component h3 {
    color: rgb(46, 39, 39); /* Warna teks hitam */
  }
  </style>
  