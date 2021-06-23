<template>
  <div class="">    
    <div class="container">
      <div>
        <p @click="plus()"><img class="icon_cart" src="~/assets/cart.png" /><sub  v-if="xx > 0"  class="sub_text_icon">{{ xx }}</sub></p>
        
        <div>
          <b-row class="start" cols="5">
            <b-col>
              <div class="">
                <button class="btn-1 bg" @click="go()">
                  <img class="img_a" src="~/assets/item_7.png" />
                  <h4 class="head_text">Space Gun LV.1</h4>
                  <p class="dis_text">
                    🔥🔥พร้อมส่ง🔥🔥<br />ยานอวกาศสุดเฟี้ยว
                  </p>
                  <span></span>
                  <p class="sub_text">20฿</p>
                </button>
              </div>
            </b-col>
            <b-col>
              <div class="">
                <button class="btn-1 bg">
                  <img class="img_a" src="~/assets/item_8.png" />
                  <h4>Space Gun LV.1</h4>
                  <p class="dis_text">
                    🔥🔥พร้อมส่ง🔥🔥<br />ยานอวกาศสุดเฟี้ยว
                  </p>
                  <span></span>
                  <p class="sub_text">20฿</p>
                </button>
              </div>
            </b-col>
            <b-col>
              <div class="">
                <button class="btn-1 bg">
                  <img class="img_a" src="~/assets/item_13.png" />
                  <h4>Space Gun LV.1</h4>
                  <p class="dis_text">
                    🔥🔥พร้อมส่ง🔥🔥<br />ยานอวกาศสุดเฟี้ยว
                  </p>
                  <span></span>
                  <p class="sub_text">20฿</p>
                </button>
              </div>
            </b-col>
            <b-col>
              <div class="">
                <button class="btn-1 bg">
                  <img class="img_a" src="~/assets/item_15.png" />
                  <h4>Space Gun LV.1</h4>
                  <span></span>
                  <p class="sub_text">20฿</p>
                </button>
              </div>
            </b-col>
            <b-col>
              <div class="">
                <button class="btn-1 bg">
                  <img class="img_a" src="~/assets/item_14.webp" />
                  <h4>Space Gun LV.1</h4>
                  <span></span>
                  <p class="sub_text">20฿</p>
                </button>
              </div>
            </b-col>
          </b-row>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export const myVar = 'This is my variable'
export const settings = {
  some: 'Settings'
}
export default {
  data() {
    return {
      xx: 0,
      
    };
  },
  methods: {
    plus() {
      this.xx = this.xx + 1 ;
      alert(this.xx);
    },
    go(){
      window.location = "index_shop";
    },
  },
};
</script>
<style>
.sub_text_icon{
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
.icon_cart {
  width: 50px;
  height: 50px;
  align-items: right ;
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
  width: 200px;
  height: 200px;
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
