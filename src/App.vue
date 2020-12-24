<template>
    <div id="app">
        <app-pizza v-bind:pizzaName='pizzaName' v-bind:pizzaPrice='pizzaPrice' v-bind:pizzaSize='pizzaSize'>
            <li>{{pizzaMainComp}}</li>
            <li>{{pizzaSecComp}}</li>
            <li>{{pizzaThirdComp}}</li>
        </app-pizza>
    </div>
</template>

<script>
import Pizza from './components/Pizza.vue'

export default {
  name: 'app',
  data(){
    return {
      pizzaName: 'ШПицца от Школы программистов',
      pizzaPrice: 600,
      pizzaSize: '30 см',
      pizzaMainComp: 'Сырокопчёные колбаски;',
      pizzaSecComp: 'Хрустящий солёный огурчик;',
      pizzaThirdComp: 'Тончайшее тесто из высшего сорта муки.'
    }
  },
  components: {
    appPizza: Pizza
  } 
}
</script>

<style>
#app {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
  background: rgb(244, 123, 186);
  background: linear-gradient(-25deg, rgba(87, 176, 255, 0.5) 20%, rgba(20, 70, 163, 0.5) 80%);
  font-family: sans-serif;
}
</style>