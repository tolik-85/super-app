<script>
import ItemVehicle from './ItemVehicle.vue'

export default {
  components: { ItemVehicle },

  props: ['vehicleType'],

  data() {
    return {
      vehicles: [],
      vehicle: { brand: '', price: 0, hasTurbo: false },
    }
  },

  methods: {
    addVehicle() {
      if (this.vehicle === '') return
      this.vehicles.push(this.vehicle)
      this.vehicle = ''
    },
  },
}
</script>

<template>
  <div>
    <h1>{{ vehicleType }}s</h1>
    <button @click="addVehicle">Add {{ vehicleType }}</button>
    <input v-model="vehicle" />
    <ul>
      <ItemVehicle
        v-for="(vehicle, idx) of vehicles"
        :key="idx"
        :vehicle="vehicle"
      />
    </ul>
  </div>
</template>
