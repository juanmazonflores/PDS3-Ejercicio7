<template>
  <div class="table-container">
    <h1>Shopping List</h1>

    <h3>Productos</h3>
    
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
</template>

<script>
export default {
  name: 'ShoppingList',
  props: ['items'],
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
  
  table {
    margin: 0 auto;
    width: 50%;
    border-collapse: collapse;
    font-size: 1rem;
    box-shadow: 0 0 20px rgba(0, 0, 0, 0.15);
  }
  
  table thead tr {
	background-color: #354a5f;
	color: #fff;
	text-align: center;
  }
  
  table thead tr th {
	border: none;
	font-size: 1.125rem;
	padding: 2rem 1.25rem;
	white-space: nowrap;
  }
  
  table tbody tr {
	border-bottom: none;
  }
  
  table tbody tr:nth-of-type(even) {
	background-color: #f3f6f9;
  }
  
  table tbody tr:last-of-type {
	border-bottom: 4px solid #354a5f;
  }
  
  table tbody tr td {
	padding: 1rem 1.25rem;
	border: none;
	white-space: wrap;
  }
  
  table tbody tr td img {
	max-width: 100px;
	height: auto;
  }
  
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
