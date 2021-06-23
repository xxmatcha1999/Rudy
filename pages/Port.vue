
<template>
  <div class="box_out">
    <p @click="plus()"><img class="icon_cart" src="~/assets/cart.png" /><sub  v-if="xx > 0"  class="sub_text_icon">{{ xx }}</sub></p>
        
    <b-row class="start">
      <b-col class="text-center">
        <div class="img">
          <img src="~/assets/pf.jpg" width="300" height="300" />
        </div>
      </b-col>
      <b-col class="font" style="padding-top: 2.5%">
        <font
          ><div class="box">
            <p>About ME</p>
            <p>I'm an internship with a passion for coding and testing.</p>
            <p>I don't have much experience with programming.</p>
            <p>But I can learn and study more to gain more experience.</p>
          </div>
        </font>
      </b-col>
    </b-row>
    <b-row class="start">
      <b-col class="">
        <div class="img">
          <h3 style="color: purple">Personal Information</h3>
        </div>
        <div >
            <ul style="list-style: none" class="arr arr_r">
                <li v-for="(value, name) in personal ">
                    {{name}}:{{ value }}
                </li>
            </ul>
        </div>
      </b-col>
      <b-col class="font" style="">
        <div class="img">
          <h3 style="color: purple">My educate</h3>
        </div>
        <div>
            <ul style="list-style: none" class="arr">
                <li v-for="(value, name) in educate ">
                    {{name}}:{{ value }}
                </li>
            </ul>
        </div>
      </b-col>
    </b-row>
    <b-row class="start">
      <b-col class="font">
       <div class="img">
          <h3 style="color: purple">Career History</h3>
        </div>
        <div>
            <ul style="list-style: none" class="arr arr_r">
                <li v-for="(value, name) in career ">
                    {{name}} - {{ value }}
                </li>
            </ul>
        </div>
      </b-col>
      <b-col class="font" style="">
        <div class="img">
          <h3 style="color: purple">Contact</h3>
        </div>
        <div>
            <ul style="list-style: none" class="arr">
                <li v-for="(value, name) in contact ">
                    {{name}} - {{ value }}
                </li>
            </ul>
        </div>
      </b-col>
    </b-row>
    <b-row class="start ">
      <b-col class="">
        <div class="img" >
          <h3 style="color: purple">Skill</h3>
        </div>
        <div >
            <ul style="list-style: none" class="arr arr_r">
                <li v-for="(value, name) in skill ">
                    {{ value }}
                </li>
            </ul>
        </div>
      </b-col>
    <b-col class="end" style="padding-bottom: 5%"></b-col>
    </b-row>
  </div>
</template> 
<script>
export default {
  
    target: 'static',
  layout: "nav",
  data() {
    return {
      personal: {
        Name: "  Napol Srisuwan",
        Nickname: "  Ham",
        Age: "  21",
        Height: "  171",
        Weight: "  78",
      },educate:{
          Study_Now:"  King Mongkut's University of Technology North Bangkok",
          High_School:"  Triamudomsuksa Suwinthawong School"
      },
      career:{
          OOP:"  Create Alien Shooter Game",
          SA:"  Create Claim Product Application",
          Com_Program:"  Create Currency Converter Program"
      },
      contact:{
          Mobile:"  0967819889",
          Facebook:"  Napol H. Sriswan",
          Line:"  nhamn"
      },
      skill:{
          1:"JAVA",
          2:"PHP",
          3:"C++",
          4:"SQL",
          5:"English"
      }
    };
  },
};
</script>
<style >
.container {
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
body {
  background-color: #80ffaa;
}
.img {
  padding-top: 5%;
  padding-left: 30%;
}
.font {
  font-size: 30;
  color: black;
}
.box {
  padding-left: 3%;
  background-color: yellow;
  margin-right: 18%;
}
.box_out {
  margin-top: 3%;
  background-color: white;
  margin-right: 18%;
  margin-left: 18%;
}
div.font {
  font-size: 150%;
}
.arr{
    font-size: 18px;

}
.arr_r{
    padding-left: 25%;
}
.end{
    margin-bottom: 5%;
}

</style>

