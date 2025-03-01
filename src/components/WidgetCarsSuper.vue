<script>
import ItemCar from './ItemCar.vue'
import AdderCar from './AdderCar.vue'

export default {
  components: { ItemCar, AdderCar },

  data() {
    return {
      cars: ['Mersedes', 'Audi'],
    }
  },

  methods: {},
}
</script>

<template>
  <div>
    <h1>Cars</h1>

    <AdderCar @car-changed="cars.push($event)" />

    <ul class="list">
      <ItemCar v-for="(car, idx) of cars" :key="idx" :car="car" />
    </ul>
  </div>
</template>
