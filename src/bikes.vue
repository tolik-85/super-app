<script>
import bikeItem from './bikeItem.vue'
export default {
  components: { bikeItem },
  data() {
    return {
      bikes: ['Dukati', 'Harley'],
      bike: '',
    }
  },
  methods: {
    handleChangeInput(e) {
      this.bike = e.target.value
    },
    handleClickButton() {
      if (this.bike === '') return
      this.bikes.push(this.bike)
      this.bike = ''
    },
  },
}
</script>
<template>
  <div>
    <button @click="handleClickButton">Add bike</button>
    <input @input="handleChangeInput" :value="bike" />
    <ul>
      <bikeItem v-for="(bike, idx) of bikes" :key="idx" :bike="bike" />
    </ul>
  </div>
</template>
