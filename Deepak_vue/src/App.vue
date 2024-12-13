<template>
  <div>
    <MyHeader heading="Goat Guns" />
    <GunBox :gun_items="gun_items" />
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue';
import GunBox from './components/GunBox.vue';

export default {
  name: 'App',
  components: {
    MyHeader, 
    GunBox,
  },
  data() {
    return {
      gun_items: []
    };
  },
  methods: {
    async fetchGunData() {
      try {
        const res = await fetch("https://guns.onrender.com/api");
        const data = await res.json();
        console.log(data);
        return data.guns;
      } catch (error) {
        console.error("Error fetching gun data:", error);
        return [];
      }
    },
  },
  async created() {
    this.gun_items = await this.fetchGunData();
  },
};
</script>

