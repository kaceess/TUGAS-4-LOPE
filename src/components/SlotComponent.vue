<!-- SlotComponent.vue -->
<template>
    <div class="slot-component">
      <h3 style="color: #ff0066;">Slot Component</h3>
      <slot></slot>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        slotData: 'Data from slot component'
      };
    }
  };
  </script>
  
  <style scoped>
  .slot-component {
    background-color: #ffcccc;
    padding: 10px;
    border-radius: 5px;
  }
  </style>
  