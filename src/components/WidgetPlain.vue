<script>
export default {
  props: ['vehicleType'],

  data() {
    return {
      vehicles: [],
      // vehicle: { brand: brand, price: price, hasTurbo: turbo },
      brand: '',
      flyDist: '1000 miles',
      plainLength: '100 meters',
    }
  },

  methods: {
    addVehicle() {
      if (this.brand === '') return
      const vehicle = {
        brand: this.brand,
        flyDist: this.flyDist,
        plainLength: this.plainLength,
      }
      this.vehicles.push(vehicle)
      this.brand = ''
      this.flyDist = '1000 miles'
      this.plainLength = '100 meters'
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
      <label for="flyDist">Введите дальность полета</label>
      <select v-model="this.flyDist" name="flyDist" id="flyDist">
        <option value="1000 miles" selected>1000 miles</option>
        <option value="2000 miles">2000 miles</option>
        <option value="3000 miles">3000 miles</option>
      </select>
    </div>
    <div class="field-wrap">
      <label for="plainLength">Введите длину самолета</label>
      <select v-model="this.plainLength" name="plainLength" id="plainLength">
        <option value="100 meters">100 meters</option>
        <option value="200 meters">200 meters</option>
        <option value="300 meters">300 meters</option>
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
        Дальность полета: {{ vehicle.flyDist }}<br />
        Длина самолета: {{ vehicle.plainLength }}<br />
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
  background: -webkit-linear-gradient(180deg, #0f0055, #4b3cff, #b4c3ff);
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
  color: rgb(255, 255, 255);
  background: transparent;
  width: 100%;
  padding: 10px 0;
  border-top: 3px solid #fff;
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
