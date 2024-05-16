<!-- ParentComponent.vue -->
<template>
  <div class="parent-component">
    <h2 style="color: #ff0066;">Parent Component</h2>
    <PinkChildComponent @childData="handleChildData" />
    <SlotComponent>
      <template v-slot:default>
        <p>Data from slot: {{ slotData }}</p>
      </template>
    </SlotComponent>
    <p>Data from child: {{ childData }}</p>
  </div>
</template>

<script>
import PinkChildComponent from './components/PinkChildComponent.vue';
import SlotComponent from './components/SlotComponent.vue';

export default {
  components: {
    PinkChildComponent,
    SlotComponent
  },
  data() {
    return {
      childData: '',
      slotData: 'Data from slot component'
    };
  },
  methods: {
    handleChildData(data) {
      this.childData = data;
    }
  }
};
</script>

<style scoped>
.parent-component {
  background-color: #ffcccc;
  padding: 20px;
  border-radius: 8px;
}
</style>
