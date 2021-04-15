<template>
 
  
   <nav class="main-menu" style="box-shadow: rgba(0, 0, 0, 0.7);">
    <div class="menu-items"><a href ="/">Best Deals</a></div> 
    <div class="menu-items"><a href="/">Pasta Pizza Party</a></div> 
    <div class="menu-items"><a href="/">Veg Pizza</a></div> 
    <div class="menu-items"><a href="/">Non-Veg Pizza</a></div> 
    <div class="menu-items"><a href="/">Meals & Combos </a></div> 
    <div class="menu-items"><a href="/">Pizza Mania</a></div> 
    <div class="menu-items"><a href="/">Speciality Chicken</a></div> 
    <div class="menu-items"><a href="/">Sides</a></div> 
    <div class="menu-items"><a href="/">Beverages</a></div> 
    <div class="menu-items"><a href="/">Dessert</a></div> 
   </nav>
   
 
</template>

<script>
export default {
    name: 'Menu',
}
</script>

<style>
.main-menu{
    background-color: white;
    color: rgba(0,0,0,0.1);
    text-transform: uppercase;
    text-decoration: none;
    white-space: nowrap;
    margin-left: 0.0em;
    margin-right: 0.3em;
    margin-top: 0.8 em;
    font-size: 0.75em;
    font-weight: 600;
    letter-spacing: 0.3px;
    text-align: center;
    cursor: pointer;
    box-shadow: rgba(0, 0, 0, 0.7);
    padding-right: 10px;
    justify-content: flex-end;

    position: fixed; /* Set the navbar to fixed position */
  top: 50px; /* Position the navbar at the top of the page */
  width: 100%; /* Full width */
width: 1475px;
  z-index: 500;

    
}
.main-menu.menu-items{border-bottom: 3px solid transparent;padding-right: 20px;}
.main-menu.menu-items.active,
.main-menu.menu-items:hover {
  
  border-bottom-color:green;
}



.menu-items a {
    text-decoration:none;
    color: rgb(180, 191, 196);
    box-shadow: rgba(0, 0, 0, 0.7);
    border-bottom-color: transparent;
}

.menu-items a:hover{
  border-bottom-color:green;
  color: blue;
  border-bottom: 3px solid green
}

</style>