
<script>
import NavBar from './NavBar.vue'
import CartItem from './CartItem.vue'

// Should inherit from app. 
export default {
    data() {
        return {
            hotdog: this.hotdog,
            quantity:0
        }
        
    },
    props: {
        hotdog: String
    },
    components: {NavBar, CartItem},

}
</script>

<template>
<header><center> THIS IS THE CART </center></header>
{{ quantity }}
<main>
  <CartItem @add-one = "()=>quantity++" @delete-one = "()=>quantity--">
  <img src="https://images.squarespace-cdn.com/content/v1/5dd8630d09ab5908e35b35a0/1574462664001-48S1VO61L9LNWNJ910CV/img-HotDogStock-1080x675.png" width="200" height="200" />
  <p>Product: Basic Hotdog</p>
  <p> This is the most basic hotdog</p>
  <p> Price: $3.00 </p>
    <button @click="() => quantity++">: add basic hotdog to cart</button>
    <button @click="() => quantity--">: delete basic hotdog from cart</button>
  </CartItem>
  <br>
  <br>
  <CartItem @add-one = "()=>quantity++" @delete-one = "()=>quantity--">
  <img src= "https://previews.agefotostock.com/previewimage/medibigoff/675a51f9f102310bc61c0ec4ec9e40b6/sfd-12991405.jpg" width="200" height="200" />
  <p>Product: Relish Hotdog</p>
  <p> This is a hotdog with relish</p>
  <p> Price: $6.00</p>
    <button @click="() => quantity++">: add relish hotdog to cart</button>
    <button @click="() => quantity--">: delete relish hotdog from cart</button>
  </CartItem>
  <br>
  <br>
  <CartItem @add-one = "()=>quantity++" @delete-one = "()=>quantity--">
      <img src="https://complex-res.cloudinary.com/image/upload/rhcvsg8mhkqdichmwew9.jpg" width="200" height="200" />
      <p>Product: Hotdog with whipped cream</p>
      <p> This hotdog has whipped cream</p>
      <p> Price: $5.00</p>
    <button @click="() => quantity++">: add whipped cream hotdog to cart</button>
    <button @click="() => quantity--">: delete whipped cream hotdog from cart</button>

  </CartItem>
  <br>
  <br>
  <CartItem @add-one = "()=>quantity++" @delete-one = "()=>quantity--">
      <img src="https://flyingcdn-cf8480cb.b-cdn.net//wp-content/uploads/2022/01/Chili-Dogs-on-a-Platter.jpg?width=800" width = "200" height = "200" />
      <p>Product: Hotdog with meat</p>
      <p> This hotdog has meat</p>
      <p> Price: $7.00</p>
      <p> {{ num }}</p>
    <button @click="() => quantity++">: add meat hotdog to cart</button>
    <button @click="() => quantity--">: delete meat hotdog from cart</button>
  </CartItem>
  <br>
  <br>
  <CartItem @add-one = "()=>quantity++" @delete-one = "()=>quantity--">
      <img src="https://www.seriouseats.com/thmb/s6XumFs3Fe4Otd8NejuSXzIVMKU=/1500x0/filters:no_upscale():max_bytes(150000):strip_icc()/__opt__aboutcom__coeus__resources__content_migration__serious_eats__seriouseats.com__recipes__images__2012__05__20120529-food-lab-cooking-sausage-hot-dog-19-e55675e3468b4189a38392ece9d77d4d.jpg" width = "200" height = "200" />
      <p>Product: Hotdog with sauerkraut</p>
      <p> This hotdog has saurkraut</p>
      <p> Price: $7.00</p>
      <p> {{ num }}</p>
    <button @click="() => quantity++">: add saurkraut hotdog to cart</button>
    <button @click="() => quantity--">: delete saurkraut hotdog from cart</button>
  </CartItem>
  <br>
  <br>
  <CartItem @add-one = "()=>quantity++" @delete-one = "()=>quantity--">
      <img src="https://assets3.thrillist.com/v1/image/2810448/1584x1056/crop;jpeg_quality=60;progressive.jpg" width = "200" height = "200" />
      <p>Product: Hotdog with ketchup</p>
      <p> This hotdog has ketchup</p>
      <p> Price: $2.00</p>
      <p> {{ num }}</p>
    <button @click="() => quantity++">: add ketchup hotdog to cart</button>
    <button @click="() => quantity--">: delete ketchup hotdog from cart</button>
  </CartItem>
  <br>
  <br>
  <CartItem @add-one = "()=>quantity++" @delete-one = "()=>quantity--">
      <img src="https://food.fnr.sndimg.com/content/dam/images/food/fullset/2010/4/13/0/GC_hot-dog-with-pickle-relish_s4x3.jpg.rend.hgtvcom.1280.720.suffix/1371592835029.jpeg" width = "200" height = "200" />
      <p>Product: Hotdog with pickles</p>
      <p> This hotdog has pickles</p>
      <p> Price: $3.00</p>
      <p> {{ num }}</p>
    <button @click="() => quantity++">: add pickle hotdog to cart</button>
    <button @click="() => quantity--">: delete pickle hotdog from cart</button>
  </CartItem>
</main>
</template>

<style scoped>
</style>

