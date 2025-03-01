<script>
export default {
  props: ['vehicleType'],

  data() {
    return {
      vehicles: [],
      // vehicle: { brand: brand, price: price, hasTurbo: turbo },
      brand: '',
      price: 0,
      passengersQty: '10 - 20',
      fuelType: 'Diesel',
    }
  },

  methods: {
    addVehicle() {
      if (this.brand === '' || this.price === '') return
      const vehicle = {
        brand: this.brand,
        price: this.price,
        passengersQty: this.passengersQty,
        fuelType: this.fuelType,
      }
      this.vehicles.push(vehicle)
      this.brand = ''
      this.price = 0
      this.passengersQty = '10 - 20'
      this.fuelType = 'Diesel'
    },
    removeVehicle(event) {
      const id = event.target.parentNode.id
      this.vehicles.splice(id, 1)
    },
  },
}
</script>

<template>
  <div class="wrapper">
    <h1>{{ vehicleType }}es</h1>
    <div class="field-wrap">
      <label for="brand">Введите бренд</label>
      <input v-model="this.brand" class="input" placeholder="Введите бренд" />
    </div>
    <div class="field-wrap">
      <label for="price">Введите цену</label>
      <input v-model.number="this.price" class="input" />
    </div>
    <div class="field-wrap">
      <label for="passengersQty">Введите колличество пассажиров</label>
      <select
        v-model="this.passengersQty"
        name="passengersQty"
        id="passengersQty"
      >
        <option value="10 - 20" selected>10 - 20</option>
        <option value="21 - 30">21 - 30</option>
        <option value="31 - 40">31 - 40</option>
      </select>
    </div>
    <div class="field-wrap">
      <label for="fuelType">Введите тип топлива</label>
      <select v-model="this.fuelType" name="fuelType" id="fuelType">
        <option value="Diesel">Diesel</option>
        <option value="Gasoline">Gasoline</option>
        <option value="Gas">Gas</option>
      </select>
    </div>
    <!-- <input
      v-model="vehicle.hasTurbo"
      class="input"
      placeholder="Введите бренд"
    /> -->
    <button @click="addVehicle" class="add-btn">Add {{ vehicleType }}</button>
    <ul class="list">
      <li
        v-for="(vehicle, idx) of vehicles"
        :key="idx"
        :vehicle="vehicle"
        class="list-item"
        :id="idx"
      >
        Бренд: {{ vehicle.brand }}<br />
        Цена: {{ vehicle.price }}<br />
        Колличество пассажиров: {{ vehicle.passengersQty }}<br />
        Тип топлива: {{ vehicle.fuelType }}<br />
        <button @click="removeVehicle" class="delete">Delete</button>
      </li>
    </ul>
  </div>
</template>
<style scoped>
h1 {
  color: #fff;
}
.wrapper {
  text-align: center;
  background: -webkit-linear-gradient(90deg, #ccbcd3, #806692, #60067e);
  border-radius: 20px;
  display: flex;
  flex-direction: column;
  gap: 10px;
  align-items: center;
}
label {
  color: #fff;
  font-size: 18px;
  margin-bottom: 5px;
}
ul {
  padding: 0;
  width: 100%;
}
.add-btn {
  font-size: 18px;
  color: white;
  background: rgb(31, 199, 143);
  padding: 5px 25px;
  border-radius: 10px;
  border: none;
}
.input,
select,
option {
  padding: 6px;
  max-width: 250px;
  width: 100%;
}
.list-item {
  font-size: 24px;
  list-style: none;
  color: rgb(0, 0, 0);
  background: transparent;
  width: 100%;
  padding: 10px 0;
  border-top: 3px solid #fff;
  /* border-bottom: 3px solid #fff;
  margin-bottom: 5px; */
}
label {
  display: block;
}
.delete {
  margin-top: 20px;
  font-size: 18px;
  color: white;
  background: tomato;
  padding: 5px 25px;
  border-radius: 10px;
  border: none;
}
</style>
