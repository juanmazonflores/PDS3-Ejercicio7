<template>
  <img alt="Shoppinglist logo" src="./assets/logo.png">
  <ShoppingList :items="items"/>
</template>

<script>
import ShoppingList from './components/ShoppingList.vue'
export default {
  name: 'App',
  components: {
    ShoppingList
  },
  data(){
    return{
      items:['shiva', 'krishna', 'ram', 'madhav']
    }
  }
}
</script>

<style>
@import '../public/styles.css';
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  align-items: center;
}
img{
  height: 200px;
}
.hello{
  align-items: center;
}
</style>
