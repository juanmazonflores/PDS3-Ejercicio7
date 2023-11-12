<template>
  <div class="hello table-container">
    <h1>Shopping List</h1>

    <h3>Productos</h3>
    <div class="table-container">
      <table>
        <thead>
          <tr>
            <th scope="col">Producto</th>
            <th scope="col">Check</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="item in items" v-bind:key="item">
            <td>
              <span>
                {{ item }}
              </span>
            </td>
            <td>
              <input type="checkbox">
            </td>
          </tr>
        </tbody>
      </table>
    </div>


  </div>
</template>

<script>
export default {
  name: 'ShoppingList',
  props: ['items'],
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
