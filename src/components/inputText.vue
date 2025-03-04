<script>
export default {
  data() {
    return {
      inputTextValue: '',
    }
  },

  // methods: {

  //   },
  // },
}
</script>

<template>
  <input
    ref="inputTextValue"
    v-model="inputTextValue"
    type="text"
    placeholder="Введите
  текст"
  />
  <p>{{ inputTextValue }}</p>
</template>
