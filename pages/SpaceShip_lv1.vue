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
                <button @click="delcart()">-</button>{{ num
                }}<button @click="addcart()">+</button>
              </p>
              <br><br>
              <button @click="plus()">ใส่ตะกร้า</button>
            </div>
            </b-col>
        </b-row>
      </b-container>
    </div>
  </div>
</template>
<script>
export const myVar = "This is my variable";
export const settings = {
  some: "Settings",
};
export default {
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
  background-color: #fff;
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

/*-------btn1--------*/
button {
  display: inline-block;
  position: relative;
  background: none;
  border: none;
  color: rgb(255, 255, 255);
  font-size: 18px;
  cursor: pointer;
  margin: 20px 30px;
  background: rgba(0, 0, 0, 0.09);
}
span {
  display: block;
  padding: 25px 80px;
}
button::before,
button::after {
  content: "";
  width: 0;
  height: 2px;
  position: absolute;
  transition: all 0.2s linear;
  background: rgb(255, 255, 255);
}

span::before,
span::after {
  content: "";
  width: 2px;
  height: 0;
  position: absolute;
  transition: all 0.2s linear;
  background: rgb(255, 255, 255);
}
button:hover::before,
button:hover::after {
  width: 100%;
}
button:hover span::before,
button:hover span::after {
  height: 100%;
}
.btn-1::before,
.btn-1::after {
  transition-delay: 0.2s;
}
.btn-1 span::before,
.btn-1 span::after {
  transition-delay: 0s;
}
.btn-1::before {
  right: 0;
  top: 0;
}
.btn-1::after {
  left: 0;
  bottom: 0;
}
.btn-1 span::before {
  left: 0;
  top: 0;
}
.btn-1 span::after {
  right: 0;
  bottom: 0;
}
.btn-1:hover::before,
.btn-1:hover::after {
  transition-delay: 0s;
}
.btn-1:hover span::before,
.btn-1:hover span::after {
  transition-delay: 0.2s;
}
</style>
