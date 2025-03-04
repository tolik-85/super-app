<script>
export default {
  data() {
    return {
      rangeValue: '',
    }
  },

  // methods: {

  //   },
  // },
}
</script>

<template>
  <div>
    <input v-model="rangeValue" type="range" min="0" max="100" />
    <p>Значение: {{ rangeValue }}</p>
  </div>
</template>
