<script>
export default {
  data() {
    return {
      dateValue: '',
    }
  },

  // methods: {

  //   },
  // },
}
</script>

<template>
  <div>
    <input v-model="dateValue" type="date" />
    <p>Значение: {{ dateValue }}</p>
  </div>
</template>
