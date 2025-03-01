<script>
export default {
  props: ['car'],
}
</script>

<template>
  <div class="list-wrapper">
    <li class="list-item">{{ car }}</li>
    <button class="delete-btn">Delete</button>
  </div>
</template>
<style scoped>
.list-item {
  list-style: none;
  font-size: 20px;
}
.delete-btn {
  color: white;
  background: tomato;
}
</style>
