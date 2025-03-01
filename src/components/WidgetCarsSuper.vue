<script>
import ItemCarSuper from './ItemCarSuper.vue'
import AdderCarSuper from './AdderCarSuper.vue'

export default {
  components: { ItemCarSuper, AdderCarSuper },

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

    <AdderCarSuper @car-changed="cars.push($event)" />

    <ul class="list">
      <ItemCarSuper v-for="(car, idx) of cars" :key="idx" :car="car" />
    </ul>
  </div>
</template>
