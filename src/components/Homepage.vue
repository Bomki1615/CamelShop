<script>
export default{
  data() {
      return {
        image: '../images/vinicius-amnx-amano-dbOV1qSiL-c-unsplash.jpg',
        url: 'https://www.vuejs.org/',
        stockDetails : [
            {
                itemNumber: 1,
                itemName : "Sweets",
                itemPrice : 5,
                itemQuantity : 30,
                itemImage: '../images/customerbox-aXq1oCCjlVM-unsplash.jpg'
            },
            {
                itemNumber: 27466,
                itemName : "Lollipop",
                itemPrice : 10,
                itemQuantity : 4,
                itemImage: '../images/jamie-albright-AHF_ZktTL6Q-unsplash.jpg'
            }
        ],
    
      }
    },
    methods(){

    },
    computed(){
        
    }
}
</script>

<template>
      <h1>My Candy Shop</h1>
    <div class="center">
        <img v-bind:src="image" width="500" height="300">
    </div>
    <div class="center">
        <a :href="url">Vue JS Practice</a>
    </div>
    <div class="center">
        <ul>
            <li v-for="(item, index) in stockDetails">
                <p>{{ item.itemName }}</p> 
                <span>Price: {{ item.itemPrice }}</span> 
                <span> Quantity: {{ item.itemQuantity }}</span>
                <span v-if = "item.itemQuantity < 10"> (Running Low!) </span>
            </li>
        </ul> 
    </div>
  
</template>

