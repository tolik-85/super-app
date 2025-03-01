<script>
export default {
  props: ['car'],
}
</script>

<template>
  <div class="list-wrapper">
    <li class="list-item">
      <b>{{ car.brand }}</b
      ><i>{{ car.price }}</i
      ><u>{{ car.isTurbo }}</u>
    </li>
    <button class="delete-btn">Delete</button>
  </div>
</template>
