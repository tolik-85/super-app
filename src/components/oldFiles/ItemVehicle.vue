<script>
export default {
  props: ['vehicle'],
}
</script>

<template>
  <li class="list-item">
    {{ vehicle }} <button @click="removeVehicle" class="delete">Delete</button>
  </li>
</template>
<style scoped>
.list-item {
  font-size: 24px;
  list-style: none;
  margin: 10px 20px;
  color: white;
}

.delete {
  margin-left: 20px;
  font-size: 18px;
  color: white;
  background: tomato;
  padding: 5px 25px;
  border-radius: 10px;
  border: none;
}
</style>
