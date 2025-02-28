<script>
import blockTitle from './blockTitle.vue'
export default {
  components: { blockTitle },
  data() {
    return {
      message: 'Hello world',
    }
  },
}
</script>
<template>
  <h1>{{ message }}</h1>
  <blockTitle />
</template>
