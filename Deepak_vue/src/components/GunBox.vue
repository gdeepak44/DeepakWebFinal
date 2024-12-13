<template>
  <div class="gun-box">
    <div v-for="gun_items of gun_items" :key="gun_items.id" class="gun-card">
      <GunList :gun_items="gun_items" />
    </div>
  </div>
</template>

<script>
import GunList from './GunList.vue';
export default {
  name: 'GunBox',
  props: {
    gun_items: Array
  },
  components: {
    GunList
  }
};
</script>

<style scoped>
.gun-box {
  display: grid;
  grid-template-columns: repeat(3, 1fr); /* 3 guns in one row */
  gap: 20px; /* Space between cards */
  padding: 20px;
}

.gun-card {
  border: 1px solid #ddd;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  overflow: hidden;
  background-color: #fff;
  text-align: center; 
}

</style>
