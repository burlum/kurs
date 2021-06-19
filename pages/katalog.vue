<template>
    <div>
    <p class="htext">В наличии</p>

<div class="input-group mb-3">
  <div class="input-group-prepend">
    <button class="btn btn-outline-secondary dropdown-toggle" type="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">Фильтр</button>
    <div class="dropdown-menu">
      <a class="dropdown-item" href="#" @click="sortParam='name'">Название A-Z</a>
      <a class="dropdown-item" href="#" @click="sortParam='namelow'">Название Z-A</a>
      <a class="dropdown-item" href="#" @click="sortParam='price'">Цена &#8743;</a>
      <a class="dropdown-item" href="#" @click="sortParam='pricelow'">Цена &#8744;</a>
    </div>
  </div>
</div>
<div class="card-deck row-cols-1 row-cols-2 row-cols-3 ">
    <div v-for="cars in sortedList" class="col mb-4" :key="cars">
    <div class="card">
      <img :src="cars.img" class="card-img-top" alt="...">
      <div class="card-body">
        <h5 class="card-title">{{cars.name}}</h5>
        <p class="card-text">{{cars.price}} руб.</p>
        <button class="btn btn-outline-dark" type="button" data-toggle="collapse" :data-target="cars.datatarget" aria-expanded="false" :aria-controls="cars.colapse">
        Характеристики
        </button>
                <div class="collapse" :id="cars.colapse">
                    <div class="spec2">
                        <img class="iconim" src="@/static/engine.png"> 
                        <div class="ctext">
                            <h5 class="card-title">Мощность</h5>
                            <p class="card-text">{{cars.HP}} Л/С</p>
                        </div>
                    </div>
                    <div class="spec2">
                        <img class="iconim" src="@/static/uskor.png"> 
                        <div class="ctext">
                            <h5 class="card-title">0-200</h5>
                            <p class="card-text"> {{cars.razgon}} сек.</p>
                        </div>
                    </div>
                    <div class="spec2">
                        <img class="iconim" src="@/static/speed.png">
                        <div class="ctext">
                            <h5 class="card-title">Макс. скорость</h5> 
                            <p class="card-text">{{cars.MS}} км/ч</p>
                        </div>
                    </div>
                </div>
      </div>
    </div>
  </div>
</div>
    </div>
</template>
<script>
import cars from '~/cars.json'
export default {
data:() =>({
    sortParam: '',
  cars:cars
}),
computed:{
            sortedList () {
                switch(this.sortParam){
                    case 'name': return this.cars.sort(sortByName);
                    case 'namelow': return this.cars.sort(sortByNameLow);
                    case 'price': return this.cars.sort(sortByPrice);
                    case 'pricelow': return this.cars.sort(sortByPriceLow);
                    default: return this.cars;
                }
             }
        }
}
var sortByName = function (d1, d2) { return (d1.name.toLowerCase() > d2.name.toLowerCase()) ? 1 : -1; };
var sortByNameLow = function (d1, d2) { return (d1.name.toLowerCase() > d2.name.toLowerCase()) ? -1 : 1; };
var sortByPrice = function (d1, d2) { return (d1.price > d2.price) ? 1 : -1; };
var sortByPriceLow = function (d1, d2) { return (d1.price > d2.price) ? -1 : 1; };

</script>
<style>
.spec2{
    display: flex;
    margin-top: 5vh;
}
.btn{
    background-color: black;
    border-color:#890000 ;
    transition: 0.2s;
    color:white;
}
.ctext{
    margin-left:2vh;
}
.card{
    position:relative;
}
</style>

