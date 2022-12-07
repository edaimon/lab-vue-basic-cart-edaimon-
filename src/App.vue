<!-- <style>
.navbar {
  text-decoration: none;
  display: flex;
  width: 100%;
  flex-direction: row;
}

</style> -->


<script>
import ITEMS from './items.json';
export default {
  data() {
    return {
      items: ITEMS,
      // Iteration 2.1
      sumaSimple: 2+2,

    };
    
  },

  methods: {
    isItEmptyCart(items) {
      return this.items.length >0 ? 'Yes' : 'No';

  }


  }
}


</script>

<template>
  <header>
    <!-- Iteration 1 -->
    <navbar class="navbar">
      
      <p>// Iteration 1</p>
      <ul>
        <li>Home</li>
        <li>Products</li>
        <li>Services</li>
        <li>Contact</li>
      </ul>
    </navbar>
  </header>
  <hr/>

  <div>
    <p>// Iteration 2.1</p>
    <p>Simple addition from variable: </p> {{ sumaSimple }}
    <hr/>
  </div>
  <div>
    <p>// Iteration 2.2</p>
    <p>Print a string reading reactive variables:</p>
    <p>Are they products in the cart? {{ isItEmptyCart() }}</p>
    
  </div>
  <hr/>
  <div>
    <p>// Iteration 3</p>
    <div v-if="(items.length < 6)">Si compras más de 6 productos, envío gratis</div> 

  </div>
  <br/>
  <hr/>
  <p>// Iteration 4</p>
  <div v-for="(item, index) of items" :key="item.uuid">
    <div>Uuid: {{ index }} | Project Name: {{ item.name }}</div>
    
  </div>
  
  <main>
   
  </main>
<hr/><br/><br/>
  <footer>@1985 Spectrum ZX corp</footer>
</template>

