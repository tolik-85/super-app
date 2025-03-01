<script>
export default {
  emits: ['car-changed'],

  data() {
    return {
      car: '',
    }
  },

  methods: {
    addCar() {
      if (this.car === '') return
      this.$emit('car-changed', this.car.trim())
      this.car = ''
      this.$refs.elInputCar.focus()
    },
  },
}
</script>

<template>
  <button @click="addCar">Add Car</button>
  <input @keypress.enter="addCar" ref="elInputCar" v-model="car" />
  <input @click="car = ''" type="button" value="x" />
</template>
