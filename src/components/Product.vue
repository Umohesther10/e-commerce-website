<template>
  <div class="product">
    <!-- <div>
      <img :src="product.imageLink" />
    </div>

    <p>{{ product.name }} {{ product.id }}</p>

    <small> &#8358; {{ product.price }} </small>

    <div>
      <button>Buy Now</button>
    </div>-->

    
    <div class="point">
      <b-card
        :to="
          `/product/${product.id}-${product.name
            .replace(/[' ']+/g, '-')
            .toLowerCase()}`
        "
      >
       <!-- img-src img-alt="Image" img-top tag="article" style="max-width: 20rem;"
        class="mb-2" > -->
        <b-img
          :src="product.imageLink"
          rounded
          alt="Rounded image"
          style="width: 200px; height: 200px; border: 2px solid #e6e6e6;"
        ></b-img>
        <b-card-text>
          <p>
            <b>{{ product.name }}</b>
          </p>
          <p>&#8358; {{ product.price }}</p>
        </b-card-text>

        <b-button :to="
          `/product/${product.id}-${product.name
            .replace(/[' ']+/g, '-')
            .toLowerCase()}`
        " href="#" variant="primary" block>Buy Now</b-button>
      </b-card>
    </div>
  </div>
</template>

<script>
export default {
  name: "Products",
  props: ["product"]
};
</script>
<style>
.product {
  display: inline-block;
  margin-left: 10px;
}
.point {
  cursor: pointer;
}
.point:hover {
  border: 1px solid rgb(238, 231, 231);
}
p {
  text-align: center;
}
</style>
