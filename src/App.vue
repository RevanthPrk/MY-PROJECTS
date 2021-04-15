<template>
  <div>
    <header>
      <i class="fa fa-bars" aria-hidden="true"></i>
      <div class="brand"><img src="https://pizzaonline.dominos.co.in/static/assets/logo_white.svg" alt=""></div>
    
     <!-- <div class="radio-btns">
  <div class="delivary-radio">
    <label class=" container1" data-label="Order_Type_Deliver">
      <span>Delivery</span>
      <input type="radio" readonly="" name="deliveryType">
      <span class="checkmark">
        <span class="checked"></span></span></label></div>
        <div class="delivary-radio"><label class="non--slctd container1" data-label="Order_Type_Pickup"><span>Pick Up/Dine-in</span><input type="radio" readonly="" name="deliveryType">
          <span class="checkmark"></span>
        </label></div>
      </div> -->
  <!-- <div class="radio-btns">
    <input type="radio">
    <span>Delivary</span></div>
   <div> <input type="radio">
    <span>Pickup</span>
  </div> -->
<div class="menuright">
      <button v-on:click="navigateTo('products')">View products</button>
      {{cart.length}} in cart
      <button v-on:click="navigateTo('cart')">View Cart</button>   
</div>  

    <div class="front-nav-links">
                    
                    
                    <div class="acc">
                        <button class="btn-link" @click="navigateTo('Login')"><span class="ti-user"></span> LOGIN </button> | <button class="btn-link" @click="navigateTo('Register')"><span class="ti-power-off"></span> REGISTER </button>
                    </div>
    </div>
    
    </header>
    <Menu /> 
    
  
    <div v-if="page === 'cart'">
      <Cart v-on:removeItemFromCart="removeItemFromCart" :cart="cart" />
    </div>

    <div v-if="page === 'products'">
      <Products v-on:addItemToCart="addItemToCart" />
    </div>
<div class="formss">
    <div v-if="page === 'Login'">
    
    <form  class="sign" @submit.prevent="handleSubmit">
      <center><h1>SIGN IN</h1></center>
    <label>Email:</label>
    <input type="email" v-model="email" required>

    <label>Password:</label>
    <input type="password" v-model="password" required>
    <div v-if="passwordError" class="error">{{ passwordError }}</div>
    <div class="submit">
      <button>LOG IN</button>
    </div>
  </form>
</div>

    <div v-if="page === 'Register'">

 <form  class="sign" @submit.prevent="handleSubmit">
   <center><h1>SIGN UP</h1></center>
    <label>Email:</label>
    <input type="email" v-model="email" required>

    <label>Password:</label>
    <input type="password" v-model="password" required>
    <div v-if="passwordError" class="error">{{ passwordError }}</div>

    <label>Role:</label>
    <select v-model="role">
      <option value="developer">CUSTOMER</option>
      <option value="designer">DRIVER</option>
    </select>

    

    <div class="terms">
      <input type="checkbox" v-model="terms" required>
      <label>Accept terms and conditions</label>
    </div>

    <div class="submit">
      <button>Create an Account</button>
    <br>
    <button v-on:click="navigateTo('Login')">Already a Member</button>
    </div>
  </form>

    </div>
</div>
     

  </div>
   <router-view/>
</template>

<script>
import Products from "./components/Products.vue";
import Cart from "./components/Cart.vue";
import Menu from './components/Menu';




export default {
  name: "App",
  data: () => {
    return {
      page: "products",

      

      cart: [],
      data:[],

    
    
    
    }
  },
  methods: {
    addItemToCart(product) {
      this.cart.push(product);
    },
    removeItemFromCart(product) {
      this.cart.splice(this.cart.indexOf(product), 1);
    },
    navigateTo(page) {
      this.page = page;
    },
    
        
        
    },
  
  
  components: { Products, Cart,Menu  }

}

</script>

<style>
body {
  margin: 0;
  background-color: rgb(242, 242, 242);
    font-family: proxima-nova, sans-serif;
  
}

</style>

<style scoped>
header {
  height: 35px;
  box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.7);
  background-color:rgb(0, 102, 167);
  text-align: right;
  font-size: 20px;
  color: #fefefe;
  padding: 0.5rem 0.9rem;
    display: flex;
    -webkit-box-align: center;
    align-items: center;
    background:  rgb(0, 102, 167);
    min-width: 14rem;
    position: fixed; /* Set the navbar to fixed position */
  top: 0; /* Position the navbar at the top of the page */
  width: 100%; /* Full width */
  overflow: hidden;
    justify-content:space-between;
    cursor: pointer;

    z-index: 500;

    
}
header button {
  padding: 10px;
  border: none;
  border-radius: 10px;
  cursor: pointer;
  color: white;
  background-color: rgb(0, 102, 167);
}
.align{
  justify-content:space-between;
  padding-right: 30px;
  color: #fefefe;
    
}
.align button{
  cursor: pointer;
}

.brand{
  display: flex;
    -webkit-box-align: center;
    align-items: center;
    padding-left: 1rem;
    margin-left: -30em;
}

.search-wrapper {
    display: flex;
    align-items: center;
}

.search-wrapper input {
    border: 0;
    outline: 0;
    padding: 1rem;
    height: 38px;
    width: 350px;
}
nav {
  display: flex;
  
    -webkit-box-pack: justify;
    justify-content:space-between;
    -webkit-box-align: center;
    align-items: center;
    height: 3.5em;
    padding: 0rem 1.5rem;
    box-shadow: rgb(210 221 233) 5px 5px 5px;
  
  
}
nav .menu-item {
  color: #FFF;
  padding: 10px 20px;
  position: relative;
  text-align: center;
  border-bottom: 3px solid transparent;
  display: flex;
  transition: 0.4s;
  color: rgb(180, 191, 196);
 box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.7);
}
nav .menu-item.active,
nav .menu-item:hover {
  background-color: #444;
  border-bottom-color: #FF5858;
  box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.7);
}
nav .menu-item a {
  color: inherit;
  text-decoration: none;
}
.nav-items{
  display: flex;
  align-items: center;
  justify-content: flex-end;  
}

.text-white{

                border: none;
                outline: none;
                height: 40px;
                flex: 1;
                padding: 1rem 1.4rem;
                border-left: 1px solid var(--text-grey);
            
}
.icon {
      cursor: pointer;
    }
    .icon-circle {
      width: 32px;
      height: 32px;
      padding: 5px;
      margin-left: 10px;
      cursor: pointer;
      color: #222;
      background-color: #fefefe;
      border-radius: 50%;
    }



  .front-nav-links {
            display: flex;
            align-items: center;
            color: #fefefe;
            padding-right: 20px;

  }

  form {
    max-width: 420px;
    margin: 30px auto;
    background:rgba(0, 0, 0, 0.1);
    text-align: left;
    padding: 40px;
    border-radius: 10px;
    margin-top: 130px;
    box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.7);
  }
  label {
    color: rgba(0, 0, 0, 0.5);
    display: inline-block;
    margin: 25px 0 15px;
    font-size: 0.6em;
    text-transform: uppercase;
    letter-spacing: 1px;
    font-weight: bold;
  }
  input, select {
    display: block;
    padding: 10px 6px;
    width: 100%;
    box-sizing: border-box;
    border: none;
    border-bottom: 1px solid #ddd;
    color: #555;
    border-radius: 5px;
  }
  input[type="checkbox"] {
    display: inline-block;
    width: 16px;
    margin: 0 10px 0 0;
    position: relative;
    top: 2px;
  }
  .pill {
    display: inline-block;
    margin: 20px 10px 0 0;
    padding: 6px 12px;
    background: #eee;
    border-radius: 20px;
    font-size: 12px;
    letter-spacing: 1px;
    font-weight: bold;
    color: #777;
    cursor: pointer;
  }
  .submit button {
    background: #0b6dff;
    border: 0;
    padding: 10px 20px;
    margin-top: 20px;
    color: white;
    border-radius: 20px;
    cursor: pointer;
  }
  .submit {
    text-align: center;
  }
  .error {
    color: #ff0062;
    margin-top: 10px;
    font-size: 0.8em;
    font-weight: bold;
  }
  .sign h1{
    color: rgba(0, 0, 0, 0.7);
    align-content: center;
    align-items: center;
  }



  .menuright{
    display: flex;
    -webkit-box-align: center;
    align-items: center;
    margin-right: -24rem;
    border-left: 1px solid rgb(0, 203, 188);
    border-right: 1px solid rgb(0, 203, 188);
    padding-left: 0.5rem;
    font-size: 15px;
  }

  .acc{
   border-left: 2px solid rgb(0, 203, 188);
   
  }
  
 
</style>
