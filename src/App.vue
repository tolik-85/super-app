<script>
import WidgetBus from './components/WidgetBus.vue'
import WidgetPlain from './components/WidgetPlain.vue'
import WidgetVehicles from './components/WidgetVehicles.vue'

export default {
  components: { WidgetVehicles, WidgetBus, WidgetPlain },
}
</script>
<template>
  <div class="container">
    <WidgetVehicles vehicle-type="Car" />

    <WidgetVehicles vehicle-type="Bike" />
    <WidgetBus vehicle-type="Bus" />
    <WidgetPlain vehicle-type="Plain" />
  </div>
</template>
<style scoped>
.container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 20px;
}
</style>

<!--

стили добавить

вместо строк объекты
удаление и редактирование транспорта
добавить автобусы
добавить самолёты
добавить корабль

добавить животных
собаки, лошади, и олени


-->
