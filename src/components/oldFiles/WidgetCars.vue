<script>
import ItemCar from './ItemCar.vue'

export default {
  components: { ItemCar },

  data() {
    return {
      cars: ['Mersedes', 'Audi'],
      car: '',
    }
  },

  methods: {
    addCar() {
      if (this.car === '') return
      this.cars.push(this.car)
      this.car = ''
    },
  },
}
</script>

<template>
  <div>
    <h1>Cars</h1>
    <button @click="addCar" class="add-car">Add Car</button>
    <input v-model="car" class="input" />
    <ul class="list">
      <ItemCar v-for="(car, idx) of cars" :key="idx" :car="car" />
    </ul>
  </div>
</template>
