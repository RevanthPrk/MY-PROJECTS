<template>
 
  <div class="container">
    <h1 style="font-family: proxima-nova, sans-serif; color:rgb(105, 129, 158);">Your Cart</h1>
    <div class="card-list">
      <div v-for="(product, index) in cart" :key="index" class="card">
        <div class="imgbox">
        <img :src="product.image" />
        </div>
        <h3>{{product.name}}</h3>
        
        <div class="cost">{{product.cost}}</div>
        <center><button v-on:click="removeItemFromCart(product)">Remove from cart</button></center>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["cart"],
  methods: {
    removeItemFromCart(product) {
      this.$emit("removeItemFromCart", product);
    }
  }
};
</script>

<style>
.card-list{
  
  background-color: #f8f4f4;
 margin-left: 65px;
 display: grid;
grid-template-columns: 1fr 1fr 1fr ;
column-gap:50px;
width:70%;
flex-flow: row nowrap;
padding-top: 200px;
row-gap:50px;
padding-left: -300px;

}
.container h1{
  margin-top: 150px;
  font-family: proxima-nova, sans-serif;
}
</style>
    