<script>
export default {
  data() {
    return {
      inputCheckboxValue1: '',
      inputCheckboxValue2: '',
      inputCheckboxValue3: '',
    }
  },

  // methods: {

  //   },
  // },
}
</script>

<template>
  <input ref="inputTextValue" v-model="inputCheckboxValue1" type="checkbox" />
  <input ref="inputTextValue" v-model="inputCheckboxValue2" type="checkbox" />
  <input ref="inputTextValue" v-model="inputCheckboxValue3" type="checkbox" />
  <div>
    <span>inputCheckboxValue1:</span>
    <p>{{ inputCheckboxValue1 }}</p>
    <span>inputCheckboxValue2:</span>
    <p>{{ inputCheckboxValue2 }}</p>
    <span>inputCheckboxValue3:</span>
    <p>{{ inputCheckboxValue3 }}</p>
  </div>
</template>
