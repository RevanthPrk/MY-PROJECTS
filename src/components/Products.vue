<template>
  
    <div class="container">
      
    <div class="product-list">
      
      
      <div v-for="(product, index) in products" :key="index" class="card">
       
       <div class="imgbox">
         
        <img :src="product.image" />
        
        <h3>{{product.cost}}</h3>
        
        </div>
       
        <h3 class="p-title">{{product.name}}</h3>
        
        <!-- <div class="disc">{{ product.disc }}</div> -->
        
        <br>
        <div class="drop">
        <h3 class="size">
            <label>Size:</label>
    <select>
      <option >Small Size</option>
      <option >Medium Size</option>
      <option >Large Size</option>
    </select>
        </h3>
        <h3 class="crust">
            <label>Crust:</label>
    <select>
      <option >New Hand Tossed</option>
      <option >Frest wheat baked</option>
      <option >Cheese burst</option>
    </select>
        </h3>
        </div>
        <button class="btn" v-on:click="addItemToCart(product)"><b>ADD TO CART</b></button>
        
          
      
    </div>
    </div>
  <div class="cart-right">
    <div class="menu-right"><img class="flsh-bnr" src="https://api.dominos.co.in/prod-olo-api/images/flashBanner/ipl_merchandizing_desktop_menu.jpeg">
    <div class="sc-dVhcbM jKybah">
      <div class="cnt ">
        <div class="sc-jwKygS kmgFYo" data-label="empty-scrn"><img src="https://pizzaonline.dominos.co.in/static/assets/empty_cart.png" srcset="https://pizzaonline.dominos.co.in/static/assets/empty_cart.png" class="img"><div class="text__wrpr"><span class="text__1">Your Cart is Empty</span><span class="text__2">Please add some items from the menu.</span></div></div></div></div></div>
  
  </div>
    </div>
</template>

<script>

export default {
  data: () => {
    return {
      products: [
        {
          name: "PANNER PIZZA",
          cost: "₹459",
          image:
            "https://images.dominos.co.in/PIZ0167.jpg",
            disc: "amazingamazingamazingamazingamazingamazingamazingamazingamazingamazing",
          
        
        },
        {
          name: "CHEESY BURST PIZZA",
          cost: "₹199",
          image:
            "https://images.dominos.co.in/new_margherita_2502.jpg",
            disc: "amazingamazingamazingamazingamazingamazingamazingamazingamazingamazing"
        },
        {
          name: "PANNER PIZZA",
          cost: "₹474",
          image:
            "https://images.dominos.co.in/farmhouse.png",
            disc: "amazingamazingamazingamazingamazingamazingamazingamazingamazingamazing"
        },
        {
          name: "PANNER PIZZA",
          cost: "₹459",
          image:
            "https://images.dominos.co.in/new_veg_extravaganza.jpg",
            disc: "amazingamazingamazingamazingamazingamazingamazingamazingamazingamazing"
        },
        {
          name: "PANNER PIZZA",
          cost: "₹399",
          image:
            "https://images.dominos.co.in/new_veggie_paradise.jpg",
            disc: "amazingamazingamazingamazingamazingamazingamazingamazingamazingamazing"
        },
        {
          name: "PANNER PIZZA",
          cost: "₹309",
          image:
            "https://images.dominos.co.in/new_cheese_n_corn.jpg",
            disc: "amazingamazingamazingamazingamazingamazingamazingamazingamazingamazing"
        },
        {
          name: "PANNER PIZZA",
          cost: "₹339",
          image:
            "https://images.dominos.co.in/CreamyTomatoPPVG_N.jpg",
            disc: "amazingamazingamazingamazingamazingamazingamazingamazingamazingamazing"
        },
        {
          name: "PANNER PIZZA",
          cost: "₹309",
          image:
            "https://images.dominos.co.in/new_cheese_n_corn.jpg",
            disc: "amazingamazingamazingamazingamazingamazingamazingamazingamazingamazing"
        },
        {
          name: "PANNER PIZZA",
          cost: "₹399",
          image:
            "https://image.freepik.com/free-photo/colorful-soda-drinks-macro-shot_53876-18225.jpg",
            disc: "amazingamazingamazingamazingamazingamazingamazingamazingamazingamazing"
        },
        {
          name: "PANNER PIZZA",
          cost: "₹129",
          image:
            "https://image.freepik.com/free-photo/tasty-italian-pizza-with-tomato-sauce-parmesan_1220-4325.jpg",
            disc: "amazingamazingamazingamazingamazingamazingamazingamazingamazingamazing"
        },
        {
          name: "PANNER PIZZA",
          cost: "₹129",
          image:
            "https://image.freepik.com/free-photo/side-view-pizza-with-salami-ham-green-peppers-tomatoes-black-olives-cheese-table_141793-2996.jpg",
            disc: "amazingamazingamazingamazingamazingamazingamazingamazingamazingamazing"
        },
        {
          name: "PANNER PIZZA",
          cost: "₹129",
          image:
            "https://image.freepik.com/free-photo/mixed-ingredient-pizza-wooden-board_114579-9317.jpg",
            disc: "amazingamazingamazingamazingamazingamazingamazingamazingamazingamazing"
        },
        {
          name: "PANNER PIZZA",
          cost: "₹309",
          image:
            "https://images.dominos.co.in/CreamyTomatoPPVG_N.jpg",
            disc: "amazingamazingamazingamazingamazingamazingamazingamazingamazingamazing"
        },
        {
          name: "PANNER PIZZA",
          cost: "₹459",
          image:
            "https://images.dominos.co.in/PIZ0167.jpg",
            disc: "amazingamazingamazingamazingamazingamazingamazingamazingamazingamazing"
        },
        {
          name: "PANNER PIZZA",
          cost: "₹359",
          image:
            "https://images.dominos.co.in/IndianTandooriPaneer.jpg",
            disc: "amazingamazingamazingamazingamazingamazingamazingamazingamazingamazing"
        },
        {
          name: "PANNER PIZZA",
          cost: "₹199",
          image:
            "https://images.dominos.co.in/new_fresh_veggie.jpg",
            disc: "amazingamazingamazingamazingamazingamazingamazingamazingamazingamazing"
        },
        {
          name: "PANNER PIZZA",
          cost: "₹259",
          image:
            "https://images.dominos.co.in/IndianTandooriPaneer.jpg",
            disc: "amazingamazingamazingamazingamazingamazingamazingamazingamazingamazing"
        },
        {
          name: "PANNER PIZZA",
          cost: "₹359",
          image:
            "https://images.dominos.co.in/CreamyTomatoPPVG_N.jpg",
            disc: "amazingamazingamazingamazingamazingamazingamazingamazingamazingamazing"
        },
        {
          name: "PANNER PIZZA",
          cost: "₹199",
          image:
            "https://images.dominos.co.in/cheesepepperoni.png",
            disc: "amazingamazingamazingamazingamazingamazingamazingamazingamazingamazing"
        },
        {
          name: "PANNER PIZZA",
          cost: "₹159",
          image:
            "https://images.dominos.co.in/CreamyTomatoPPVG_N.jpg",
            disc: "amazingamazingamazingamazingamazingamazingamazingamazingamazingamazing"
        },
        {
          name: "PANNER PIZZA",
          cost: "₹199",
          image:
            "https://images.dominos.co.in/cheese_and_tomato.png",
            disc: "amazingamazingamazingamazingamazingamazingamazingamazingamazingamazing"
        },
        {
          name: "PANNER PIZZA",
          cost: "₹349",
          image:
            "https://images.dominos.co.in/new_non_veg_supreme.jpg",
            disc: "amazingamazingamazingamazingamazingamazingamazingamazingamazingamazing"
        },
        {
          name: "PANNER PIZZA",
          cost: "₹499",
          image:
            "https://images.dominos.co.in/new_chicken_fiesta.jpg",
            disc: "amazingamazingamazingamazingamazingamazingamazingamazingamazingamazing"
        },
        {
          name: "PANNER PIZZA",
          cost: "₹359",
          image:
            "https://images.dominos.co.in/updated_achari_do_pyaza.jpg",
            disc: "amazingamazingamazingamazingamazingamazingamazingamazingamazingamazing"
        }
        
      ]
    };
  },
  methods: {
    addItemToCart(product) {
      this.$emit("addItemToCart", product);
    }
  },

};
</script>

<style>




.product-list{
  
  background-color: #f8f4f4;
 margin-left: 65px;
 display: grid;
grid-template-columns: 1fr 1fr 1fr;
column-gap:50px;
width:70%;
flex-flow: row nowrap;
padding-top: 200px;
row-gap:50px;

}
.container{
  background-color: #f8f4f4;
  width:100%;
  display: flex;
  flex-flow: row nowrap;
}
.cart-right{
  margin-top: 160px;
  margin-right: 50px;
  background-color: #f8f4f4;
  width:30%;
  flex-flow: cloumn nowrap;
  height: 50px;


}
.cnt {
    margin-top: 1rem;
    position: relative;
    min-height: 28rem;
    max-height: 60vh;
    width: 20rem;
    background: rgb(255, 255, 255);
    overflow-y: auto;
    transition: all 1s ease 0s;
    box-shadow: rgb(0 0 0 / 12%) 0px 2px 2px 0px, rgb(0 0 0 / 12%) 0px 2px 4px 0px;
    margin-left: 35px;
    position: fixed;
}
.kmgFYo {
    display: flex;
    flex-direction: column;
    -webkit-box-align: center;
    align-items: center;
    -webkit-box-pack: center;
    justify-content: center;
    height: 100%;
    padding: 0px 1rem;
    margin-left: 150px;
}
.card{
  background-color: white;
  border-radius: 4px;
  
  box-shadow: 2px 2px 5px rgba(0, 0, 20, 0.4) ;
  text-align: center;
  width:290px;
  height:350px;
  

  

}

.flsh-bnr{
  width: 320px;
  height: 120px;
  margin-left: 38px;
}

.text__1{
  font-size: 1.5rem;
    font-weight: 900;
    text-transform: uppercase;
    color: rgb(113, 128, 145);
    width: 100%;
    display: flex;
}
.text__2{
  font-size: 1rem;
    color: rgb(105, 129, 158);
    padding-top: 0.2rem;
    width: 100%;
    display: flex;
}
.text__wrpr {
    -webkit-box-align: center;
    align-items: center;
    z-index: 1;
    display: flex;
    flex-direction: column;
    width: 90%;
    margin-top: 6rem;
    }

.p-title{
font-size: 15px;
font-weight: bold;
left: -100px;
color: rgba(0, 0, 0, 0.9);
}




/* .card.disc{
  text-align: left;
  margin-left: 2em;
  margin-bottom: 0.5em;
  width:270px;
  text-align: justify;
} */

.btn{
background-color: #f8f4f4;

border-radius: 5px;
padding: 0.5em;
justify-content: end;

float:right;
margin-right: 10px;
margin-bottom: 10px;

}
button {
    cursor: pointer;
    padding: 0.433rem;
    border: 1px solid rgb(0, 171, 0);
    color: rgb(0, 171, 0);
    background-color: rgb(255, 255, 255);
}
.imgbox img{
  width:290px;
height: 145px;
border-top-left-radius: 3px;
border-top-right-radius: 3px;
}
.imgbox{
  position: relative; 
   width: 100%;
}
.imgbox h3 { 
   position: absolute; 
   top: 100px; 
   left: -110px; 
   width: 100%; 
   color: white;
    
}

  .card select {
    display: flex;
    padding: 10px 6px;
    flex-flow: column nowrap;
    box-sizing: border-box;
    border: none;
    border-bottom: 2px solid #ddd;
    color:rgba(0, 0, 0, 0.9);
    font-weight: bold;
    border-radius: 5px;
    align-items: center;
    font-size: 11px;
    font-family: proxima-nova, sans-serif;
    margin-left: 6px;
  }

  label {
    color: rgb(180, 191, 196);
    display: flex;
    align-items: center;
    margin-left: 20px;
    font-size: 0.6em;
    font-family: proxima-nova, sans-serif;
    letter-spacing: 1px;
    font-weight: bold;
    column-gap:30px;
    margin-right: 4px;
  }
.size{
  flex-flow: cloumn nowrap;
  width: 40%;
  right:10px;
}
.crust{
  flex-flow: cloumn nowrap;
  width: 60%;
}

select options{
  display: flex;
  font-size: 10px;
}
.drop{
  flex-basis: auto;
    flex-flow: row nowrap;
    display: flex;
    margin-top: -0.9rem;
    margin-bottom:1.0rem;
    width: 100%;
    align-items: center;
    column-gap: 38px;
   border-top: 0.1px solid rgb(180, 191, 196);
   font-size: 17px;
   color: rgb(180, 191, 196);
   height: 75px;
   font-family: proxima-nova, sans-serif;
}

 
    
    
</style>