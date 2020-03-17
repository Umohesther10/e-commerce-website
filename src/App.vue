<template>
  <div id="app">
    <Header />
    <div class="root">
      <b-container class="bv-example-row" fluid>
        <b-row>
          <b-col cols="4">
            <h4>Categories</h4>
            <hr />
            <div class="sticky">
              <Category v-for="section in categories" :category="section" :key="section.id" />
            </div>
          </b-col>
          <b-col cols="8">
            <h3>Product Catalogue</h3>
            <hr />
            <Product v-for="item in products" :product="item" :key="item.id" />
          </b-col>
        </b-row>
      </b-container>
    </div>
  </div>
</template>


<script>
import Product from "@/components/Product.vue";
import Category from "@/components/Category.vue";
import Header from "@/components/Header.vue";
export default {
  name: "App",
  data() {
    return {
      products: [
        {
          id: 1,
          name: "Curly wig",
          price: "22,000",
          imageLink: require("./assets/wig2.jpg")
        },
        {
          id: 2,
          name: "Baby Hanger",
          price: "9,000",
          imageLink: require("./assets/hanger2.jpg")
        },
        {
          id: 3,
          name: "I Phone 11",
          price: "289,000",
          imageLink: require("./assets/iphone.jpg")
        },
        {
          id: 4,
          name: "Fridge",
          price: "223,000",
          imageLink: require("./assets/fridge.jpg")
        },
        {
          id: 5,
          name: "Men shoes",
          price: "15,000",
          imageLink: require("./assets/shoe.jpg")
        },
        {
          id: 6,
          name: "Gown",
          price: "6,000",
          imageLink: require("./assets/female dress.jpg")
        },
        {
          id: 7,
          name: "Sneaker",
          price: "10,000",
          imageLink: require("./assets/sneakers.jpg")
        },
        {
          id: 8,
          name: "Shirts",
          price: "5,000",
          imageLink: require("./assets/shirt.jpg")
        },
        {
          id: 9,
          name: "HP Elite Book",
          price: "150,000",
          imageLink: require("./assets/hp.jpg")
        },
        {
          id: 10,
          name: "Necklace",
          price: "2,000",
          imageLink: require("./assets/necklace.jpg")
        },

        {
          id: 7,
          name: "Court Heels",
          price: "8,000",
          imageLink: require("./assets/heel.jpg")
        },

        {
          id: 9,
          name: "Mac Book Pro",
          price: "350,000",
          imageLink: require("./assets/mac.jpg")
        }
      ],
      categories: [
        {
          id: "1",
          name: `Weavons and wigs`
        },
        {
          id: "2",
          name: `Baby Accessories`
        },
        {
          id: "3",
          name: `Phones`
        },
        {
          id: "4",
          name: `Electronics`
        },
        {
          id: "5",
          name: `Men shoes`
        },
        {
          id: "6",
          name: `Women Dresses`
        },
        {
          id: "7",
          name: `Women Shoes`
        },
        {
          id: "8",
          name: `Men Clothes`
        },
        {
          id: "9",
          name: `Laptops`
        },
        {
          id: "10",
          name: `Accessories`
        }
      ]
    };
  },
  components: {
    Product,
    Header,
    Category
  }
};
</script>

<style>
.root {
  margin-top: 80px;
}
.sticky {
  position: -webkit-sticky;
  position: sticky;
  top: 0;
}
/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
} */
</style>
