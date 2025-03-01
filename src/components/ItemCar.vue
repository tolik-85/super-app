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
