<script>
import carItem from './carItem.vue'
import bikeItem from './bikeItem.vue'
export default {
  components: { carItem, bikeItem },
  data() {
    return {
      cars: ['Mersedes', 'Audi'],
      car: '',
      bikes: ['Dukati', 'Harley'],
      bike: '',
    }
  },
  methods: {
    handleChangeInput(e) {
      this.car = e.target.value
    },
    handleClickButton() {
      if (this.car === '') return
      this.cars.push(this.car)
      this.car = ''
    },
  },
}
</script>
<template>
  <div>
    <button @click="handleClickButton">Add Car</button>
    <input @input="handleChangeInput" :value="car" />
    <ul>
      <carItem v-for="(car, idx) of cars" :key="idx" :car="car" />
    </ul>
  </div>
</template>
