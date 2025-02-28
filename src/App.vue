<script>
import WidgetVehicles from './components/WidgetVehicles.vue'

// import WidgetBikes from './components/WidgetBikes.vue'
// import WidgetCars from './components/WidgetCars.vue'

export default {
  // components: { WidgetCars, WidgetBikes },

  components: { WidgetVehicles },
}
</script>
<template>
  <div>
    <WidgetVehicles vehicle-type="Car" />

    <WidgetVehicles vehicle-type="Bike" />
  </div>
</template>

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
