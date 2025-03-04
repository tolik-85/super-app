<script>
export default {
  emits: ['car-changed'],

  data() {
    return {
      car: {
        brand: null,
        price: 0,
        isTurbo: false,
      },
    }
  },

  methods: {
    addCar() {
      if (this.car.brand === '') return
      this.$emit('car-changed', this.car)
      this.car = {
        brand: '',
        price: 0,
        isTurbo: false,
      }
    },
  },
}
</script>

<template>
  <button @click="addCar">Add Car</button>
  <input v-model="car.brand" />
  <input v-model="car.price" />
  <input v-model="car.isTurbo" />
  <input @click="car = ''" type="button" value="x" />
</template>
