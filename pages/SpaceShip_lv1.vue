<template>
  <div class="">
    <div class="container">
      <b-container>
        <b-row >
          <b-col cols="8"
            ><div>
              <p>
                <img class="icon_cart" src="~/assets/cart.png" /><sub
                  v-if="cart > 0"
                  class="sub_text_icon"
                  >{{ cart }}</sub
                >
              </p>
            </div>
          </b-col>

          <b-col>
            <div>
              <img class="img_a" src="~/assets/item_7.png" />
            </div>
          </b-col>
          <b-col>
            <div class="information">
              <h1>Space Ship Level 1</h1>
              <p>🔥🔥พร้อมส่ง🔥🔥<br />ยานอวกาศสุดเฟี้ยว</p>
              <p>
                <button  @click="delcart()" class="btn btn-primary tab" >-</button>
                {{ num }}
                <button @click="addcart()" class="btn btn-primary">+</button>
              </p>
              <br><br>
              <button @click="plus()"  class="btn btn-primary">ใส่ตะกร้า</button>
            </div>
            </b-col>
        </b-row>
      </b-container>
    </div>
  </div>
</template>
<script>

export default {
  layout:'nav_shop',
  data() {
    return {
      cart: 0,
      a: 0,
      num: 0,
    };
  },
  mounted() {
    if (localStorage.cart) {
      this.a = localStorage.getItem("cart");
      this.cart = parseInt(this.a);
    }
  },
  methods: {
    plus() {
      this.cart = this.cart + this.num;
      localStorage.setItem("cart", JSON.parse(this.cart));
      alert("เพิ่มลงตะกร้าเรียบร้อย");
    },
    go() {
      window.location = "Me";
    },
    addcart() {
      this.num = this.num + 1;
    },
    delcart() {
      this.num = this.num - 1;
    },
  },
};
</script>
<style>
.tab { 
       display:inline-block; 
       margin-left: 40px; 
}
.sub_text_icon {
  font-size: 30px;
}
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
.information {
  text-align: left;
  font-size: 26px;
  color: red;
  background: none;
  background-color: rgba(255, 255, 255, 0.123);
  padding-left: 3%;
  padding-right: 3%;
  padding-top: 2%;
  padding-bottom: 2%;
  border-radius: 5%;
}
.icon_cart {
  width: 50px;
  height: 50px;
  align-items: right;
  text-align: right;
}
.bg:hover {
  outline-color: red;
}
.head_text {
  color: white;
}
.dis_text {
  color: white;
  text-align: left;
  font-size: 15px;
}
.sub_text {
  text-align: left;
  font-size: 20px;
  color: red;
}
.sub_text_icon {
  text-align: right;
  font-size: 20px;
  color: red;
}
.bg_item {
  background-image: url("assets/bg_item.png");
}
.bg_f {
  background-color: #3c20d8;
}
.bg_g {
  background-color: #dd3a42;
  color: white;
}
.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}
.img_a {
  width: 500px;
  height: 500px;
  text-align: left;
}
.links {
  padding-top: 15px;
}

body {
  background-image: url("assets/bg2.jpg");
  background-color: #e9e9e9;
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-size: 100% 100%;
}

</style>