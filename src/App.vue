<template>
Horse power:
<input v-model="car.horsePower"/>
<br>

Price:
<input v-model="car.price"/>
<br>

 Plate number 
 <span class="plateNumber">
   {{ car.plateNumber }}
   </span>
 <br/>

 Horse power
 <span class="hp">
   {{ car.horsePower }}
   </span>
<br/>

Kāda ir Edvarda mašīna? = 
<span class="monster" v-if="isCoolCar(car)">
  Ahujena
</span>

<br>

Lēta mašīna? = 
<span class="leti" v-if="carsPrice(car)">
  Nice
</span>

</template>

<script>
export default {
  data () {
    return {
      car: {
        plateNumber: "AA-3333",
        horsePower: 1200,
        price: 199,        
      }
    }    
  },
  methods: {
    isCoolCar (car) {
      return (car.horsePower > 1000)
    },
    carsPrice (car) {
      return (car.price < 200)
    }
  }
}
</script>

<style>
.plateNumber {
  color: red;
  font-weight: bold;
  }
.hp {
  color: blue;
  font-weight: bold;
  }
.leti {
  color: green;
  font-weight: bold;
}

.monster{
  color: magenta;
  font-weight: bold;
}
</style>
