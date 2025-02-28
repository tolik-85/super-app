<script>
import ItemBike from './ItemBike.vue'

export default {
  components: { ItemBike },

  data() {
    return {
      bikes: ['Dukati', 'Harley'],
      bike: '',
    }
  },

  methods: {
    addBike() {
      if (this.bike === '') return
      this.bikes.push(this.bike)
      this.bike = ''
    },
  },
}
</script>

<template>
  <div>
    <h1>Bikes</h1>
    <button @click="addBike">Add bike</button>
    <input v-model="bike" />
    <ul>
      <ItemBike v-for="(bike, idx) of bikes" :key="idx" :bike="bike" />
    </ul>
  </div>
</template>
