<template>
  <div class="gun-list">
    <img :src="gun_items.gun_image" alt="gun img" class="gun-image" />
    <div class="data-gun">
      <h3><b>Gun Name: {{ gun_items.gun_name }}</b></h3>
      <h4>Gun Cost: {{ gun_items.cost }}</h4>
      <h4>Gun Type Left: {{ gun_items.Gun_type }}</h4>
      <h4>Ammo: {{ gun_items.ammo }}</h4>
      <h4>Range: {{ gun_items.range }}</h4>
    </div>
  </div>
</template>

<script>
export default {
  name: "GunList",
  props: {
    gun_items: Object
  }
};
</script>

<style scoped>
.gun-list {
  text-align: center;
  padding: 10px;
}

.gun-image {
  width: 200px; 
  height: 150px; 
  object-fit: cover; 
  border-radius: 8px;
  margin: 0 auto;
}

.data-gun h3,
.data-gun h4 {
  margin: 5px 0;
}
</style>
