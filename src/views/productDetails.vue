<template>
  <div class="detail">
    <b-container class="bv-example-row">
      <b-row>
        <b-col>
          <div style="margin-bottom:20px;">
            <b-img
              :src="`${picture}`"
              fluid
              alt="Responsive image"
              style="width:200px; height: 200px; border: 1px; solid; grey;"
            ></b-img>
          </div>
          <span v-for="img in productItem[0].image" :key="img.image" style="padding:10px;">
            <b-img :src="img" fluid alt="Responsive image" id="small" @click="change(img)"></b-img>
          </span>
          <hr />
        </b-col>
        <b-col cols="6">
          <div>
            <h5>
              <div id="icon">
                <i id="ico" class="fas fa-heart"></i>
              </div>
              {{productItem[0].name}}
            </h5>
            <hr />

            <h6>&#8358; {{ productItem[0].price }}</h6>
            <hr />

            <b-button href="#" variant="primary" block>
              ADD TO CART
              <div id="cart">
                <i class="fas fa-cart-plus"></i>
              </div>
            </b-button>
          </div>
        </b-col>

        <b-col>
          <div>
            <b-jumbotron fluid="false" style="color: blue">
              <template v-slot:lead>DELIVERY AND RETURN</template>

              <hr />
              <b-row>
                <b-col cols="2">
                  <i id="ic" class="fas fa-shipping-fast"></i>
                </b-col>
                <b-col>
                  Delivery Information
                  Normally delivered between 2-7 working days, Please check the exact delivery time.
                </b-col>
              </b-row>
            </b-jumbotron>
          </div>
        </b-col>
      </b-row>
      <b-row>
        <b-col>
          <div>
            <h4 style="color: blue">Product Details</h4>
            <hr />
            <h6>{{productItem[0].detail}}</h6>
          </div>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
export default {
  name: "productDetails",
  data() {
    return {
      productItem: [],
      picture: null,
      products: [
        {
          id: 1,
          name: "WATER WAVES Cambodian Weave Bundle For Beautiful Ladies",
          price: "22,000",
          detail:
            "It a quality human hair wig, it is made with good human hair blend, it has a soft texture, it doesn't tangle and it doesn't shed it doesn't rough and it doesn't change colour, it can be dyed, and it can be bleached, it doesn't change colour and it doesn't rough, it can be washed, it is the people's choice, it is the type of wig you will love to own, it is not common, it is can be used for both ladies and slay Mama's, it can be used for both casual and parties, it is recommendable, it gives a difference look, it is very easy to maintain, it can be maintained with ordinary water or good human hair spray, it lasts longerit is the type of wig you will love to order for your friends our products has no rival,all our products are quality guaranteed. ",
          imageLink: require("../assets/wig2.jpg"),
          image: [
            require("../assets/wig2.jpg"),
            require("../assets/wig4.jpg"),
            require("../assets/wig5.jpg")
          ]
        },

        {
          id: 2,
          name: "Baby Clothes Hanger",
          price: "9,000",
          detail:
            "These baby closet hangers are suitable for hanging clothes from newborn sizing to 2T. Great desgin:baby hangers have the little hook on either side to help keep clothes in place.The slot is great for pants/shorts, baby hangers for closet are also wide enough to actually fit pants under a shirt or jacket hanging over.",
          imageLink: require("../assets/hanger2.jpg"),
          image: [
            require("../assets/hanger2.jpg"),
            require("../assets/b1.jpg"),
            require("../assets/b2.jpg")
          ]
        },
        {
          id: 3,
          name: "Apple IPhone 11 64GB Black - Authorized Reseller Store",
          price: "289,000",
          detail:
            "The iPhone 11 features an Intel modem chip with Gigabit-class LTE, 2x2 MIMO, and LAA, Wi-Fi 6 support (802.11ax) with 2x2 MIMO, Bluetooth 5.0, Dual-SIM with eSIM, and an Apple-designed U1 Ultra Wideband chip that improves spatial awareness and allows for better indoor tracking.",
          imageLink: require("../assets/iphone.jpg"),
          image: [
            require("../assets/iphone.jpg"),
            require("../assets/p2.jpg"),
            require("../assets/p3.jpg")
          ]
        },
        {
          id: 4,
          name:
            "Haier Thermocool 180-Litre Double Door Refrigerator- HRF 180EX",
          price: "223,000",
          detail:
            "A refrigerator (colloquially fridge) consists of a thermally insulated compartment and a heat pump (mechanical, electronic or chemical) that transfers heat from the inside of the fridge to its external environment so that the inside of the fridge is cooled to a temperature below the room temperature.",
          imageLink: require("../assets/fridge.jpg"),
          image: [
            require("../assets/fridge.jpg"),
            require("../assets/f1.jpg"),
            require("../assets/f2.jpg")
          ]
        },
        {
          id: 5,
          name: "MENS FORMAL OXFORD SHOES",
          price: "15,000",
          detail:
            "Durable and flexible: the stripe pattern on the sole is designed to be non-slip and flexible. Our shower slippers are very soft and flexible, designed to fit your feet perfectly, allowing you to enjoy the comfort of these slippers for a long time.",
          imageLink: require("../assets/shoe.jpg"),
          image: [
            require("../assets/shoe.jpg"),
            require("../assets/s1.jpg"),
            require("../assets/s2.jpg")
          ]
        },
        {
          id: 6,
          name: "Women's Dresses Pleated Ladies Fashion Dress",
          price: "6,000",
          detail:
            "Lovely Pleated gownQuality unique outfit from dexterous wears, made of high quality material, Very cute fitted and attractive outfit that makes you look gorgeous and adorable, All dexterous wears outfit are durable and of high quality yet very affordable, don’t miss this outfit, just go ahead and purchase and you will be glad you did.Stand out in this midi length belted dress made from carefully selected top quality fabrics. The self belt complements to give a perfect finishing..What other way to look stunning than this midi length dress that can be styled as corporate, casual or church outfit. Whatever way you choose to style this outfit, be sure to have the spot light on you when you step out in this gorgeous piece.",
          imageLink: require("../assets/female dress.jpg"),
          image: [
            require("../assets/female dress.jpg"),
            require("../assets/d1.jpg"),
            require("../assets/d2.jpg")
          ]
        },
        {
          id: 7,
          name: "Elegant Designer Athletic Sneakers ",
          price: "10,000",
          detail:
            "Suitable for all seasons, indoor bedrooms, bathrooms, living rooms, spas, gyms, swimming pools, beaches, vacations, leisure, public showers, steam rooms, dormitories, camps, swimming pools, changing rooms.",
          imageLink: require("../assets/sneakers.jpg"),
          image: [
            require("../assets/sneakers.jpg"),
            require("../assets/sn3.jpg"),
            require("../assets/slide1.jpg")
          ]
        },
        {
          id: 8,
          name: "Mens Coporate Shirts",
          price: "5,000",
          detail:
            "There are lots of powerful inspiration behind everything we design. We are inspired by you. Chrysolite Designs is a fashion brand that uses textile designs to connect mind & soul together.",
          imageLink: require("../assets/shirt.jpg"),
          image: [
            require("../assets/shirt.jpg"),
            require("../assets/ms1.jpg"),
            require("../assets/ms2.jpg")
          ]
        },
        {
          id: 9,
          name: "HP Elite Book",
          price: "150,000",
          detail:
            "This laptop is designed to last as you will be wowed by its ability to relieve you of all your school, office or other personal services as you so desire. ",
          imageLink: require("../assets/hp.jpg"),
          image: [
            require("../assets/hp.jpg"),
            require("../assets/h1.jpg"),
            require("../assets/h2.jpg")
          ]
        },
        {
          id: 10,
          name: "Attain Glory To Plate Precious Stone Necklace",
          price: "5,000",
          detail:
            "A one stop destination for that perfect outfit or accessory no matter what the occasion. ",
          imageLink: require("../assets/necklace.jpg"),
          image: [
            require("../assets/necklace.jpg"),
            require("../assets/n1.jpg"),
            require("../assets/n2.jpg")
          ]
        },

        {
          id: 11,
          name: "Forever 21 Black Colour",
          price: "8,000",
          detail:
            "Women everywhere know all too well the unbearable pain experienced after a long day or night in high heels, or the discomfort that comes when breaking in a new pair of shoes. ",
          imageLink: require("../assets/heel.jpg"),
          image: [
            require("../assets/heel.jpg"),
            require("../assets/c1.jpg"),
            require("../assets/c2.jpg")
          ]
        },

        {
          id: 12,
          name:
            "Apple Macbook Pro 15.4 2.9GHZ - 1TB SSD -32GB Ram - Core I9 - Model 2018 Touch Bar (MR952LL/A)",
          price: "350,000",
          detail:
            "It is powered by a Core i9 processor and it comes with 32GB of RAM. The Apple MacBook Pro packs 512GB of SSD storage. Connectivity options include Wi-Fi 802.11 ac, Bluetooth and it comes with 2 USB ports (2 x USB 3.0), Mic In ports.",
          imageLink: require("../assets/mac.jpg"),
          image: [
            require("../assets/mac.jpg"),
            require("../assets/m1.jpg"),
            require("../assets/m2.jpg")
          ]
        }
      ]
    };
  },
  created() {
    this.productItem = this.products.filter(item => {
      return item.id === parseInt(this.$route.params.id);
    });
    // console.log(this.productItem);
    this.picture = this.productItem[0].imageLink;
  },

  methods: {
    change: function(image) {
      this.picture = image;
    }
  }
};
</script>
<style scoped>
#small {
  width: 50px;
  height: 50px;
  border: 1px solid black;
}
#small:hover {
  border: 2px solid #0373fc;
  cursor: pointer;
}
#cart {
  float: left;
  color: white;
  font-size: 20px;
}
.detail {
  margin-top: 70px;
  padding-top: 20px;
}
#icon {
  float: right;
}
#ico {
  color: #0373fc;
}
#ic {
  color: #0373fc;
  font-size: 20px;
}
</style>
