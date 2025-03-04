<script>
export default {
  data() {
    return {
      selectedRadio: '',
    }
  },

  // methods: {

  //   },
  // },
}
</script>

<template>
  <div>
    <label
      ><input v-model="selectedRadio" type="radio" value="A" /> Вариант A</label
    >
    <label
      ><input v-model="selectedRadio" type="radio" value="B" /> Вариант B</label
    >
    <label
      ><input v-model="selectedRadio" type="radio" value="C" /> Вариант C</label
    >

    <p>Выбрано: {{ selectedRadio }}</p>
  </div>
</template>
