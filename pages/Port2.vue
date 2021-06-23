<template>
  <div>
    <div>
      <b-row class="start">
        <b-col class="text-center">
          <div style="padding-top: 25px">
            <img src="~/assets/pf.jpg" width="250" height="250" />
          </div>
        </b-col>
      </b-row>
      <b-row class="start">
        <b-col class="font text-center" style="padding-top: 2.5%">
          <font
            ><div class="">
              <p>About ME</p>
              <p>I'm an internship with a passion for coding and testing.</p>
              <p>I don't have much experience with programming.</p>
              <p>But I can learn and study more to gain more experience.</p>
            </div>
          </font>
        </b-col>
      </b-row>
      <b-row class="">
        <b-col class="font text-center" style="padding-top: 2.5%">
          <div
            v-if="tag_updown == true"
            data-toggle="collapse"
            href="#multiCollapseExample1"
          >
            <div >
              <ul style="list-style: none" class="arr">
                <li v-for="(value, name) in educate">{{ name }}:{{ value }}</li>
              </ul>
            </div>
          </div>
          <div
            
            v-if="tag_updown2 == true"
            data-toggle="collapse"
            href="#multiCollapseExample1"
          >
            <div>
              <ul style="list-style: none" class="arr arr_r">
                <li v-for="(value, name) in personal">
                  {{ name }}:{{ value }}
                </li>
              </ul>
            </div>
          </div>
          <div
            v-if="tag_updown3 == true"
            data-toggle="collapse"
            href="#multiCollapseExample1"
          >
            <div >
              <ul style="list-style: none" class="arr arr_r">
                <li v-for="(value, name) in career">
                  {{ name }} - {{ value }}
                </li>
              </ul>
            </div>
          </div>
        </b-col>
        <b-col
          cols="12"
          md="auto"
          class="font text-center"
          style="padding-top: 2.5%"
        >
          <b-button
            pill
            variant="outline-danger"
            class="col bg-white p-2"
            v-if="tag_updown == false"
            @click="switchiconna()"
            data-toggle="collapse"
            >Personal Information</b-button
          >
          <b-button
            pill
            variant="outline-danger"
            class="col bg-white p-2"
            v-if="tag_updown == true"
            @click="switchiconna()"
            data-toggle="collapse"
            >Personal Information</b-button
          >
        </b-col>
        <b-col col lg="2" class="font text-center" style="padding-top: 2.5%">
          <b-button
            pill
            variant="outline-danger"
            class="col bg-white p-2"
            v-if="tag_updown == false"
            @click="switchiconna2()"
            data-toggle="collapse"
            >My educate</b-button
          >
          <b-button
            pill
            variant="outline-danger"
            class="col bg-white p-2"
            v-if="tag_updown == true"
            @click="switchiconna2()"
            data-toggle="collapse"
            >My educate</b-button
          >
        </b-col>
        <b-col col lg="2" class="font text-center" style="padding-top: 2.5%">
          <b-button
            pill
            variant="outline-danger"
            class="col bg-white p-2"
            v-if="tag_updown == false"
            @click="switchiconna3()"
            data-toggle="collapse"
            >Career History</b-button
          ><b-button
            pill
            variant="outline-danger"
            class="col bg-white p-2"
            v-if="tag_updown == true"
            @click="switchiconna3()"
            data-toggle="collapse"
            >Career History</b-button
          >
        </b-col>
      </b-row>
      <br />
      <br />
      <b-row class="start">
        <b-col class="text-center"
          ><img src="~/assets/skill.png" width="80" height="80"
        /></b-col>
        <b-col class="text-center"
          ><img src="~/assets/java.jpg" width="60" height="60"
        /></b-col>
        <b-col class="text-center"
          ><img src="~/assets/php.png" width="60" height="60"
        /></b-col>
        <b-col class="text-center"
          ><img src="~/assets/c.png" width="60" height="60"
        /></b-col>
        <b-col class="text-center"
          ><img src="~/assets/sql.png" width="60" height="60"
        /></b-col>
      </b-row>
      <b-row class="start">
        <b-col class="font text-center" style="padding-top: 2.5%">
          <h3 style="color: purple">Contact</h3>

          <div>
            <ul style="list-style: none" class="arr">
              <li v-for="(value, name) in contact">{{ name }} - {{ value }}</li>
            </ul>
            .
          </div>
        </b-col>
      </b-row>
    </div>
  </div>
</template>
<script>
export default {
  target: "static",
  layout: "nav",
  data() {
    return {
      tag_updown: false,
      tag_updown2: true,
      tag_updown3: false,
      tag_updown4: false,
      show: false,
      personal: {
        Name: "  Napol Srisuwan",
        Nickname: "  Ham",
        Age: "  21",
        Height: "  171",
        Weight: "  78",
      },
      educate: {
        Study_Now: "  King Mongkut's University of Technology North Bangkok",
        High_School: "  Triamudomsuksa Suwinthawong School",
      },
      career: {
        OOP: "  Create Alien Shooter Game",
        SA: "  Create Claim Product Application",
        Com_Program: "  Create Currency Converter Program",
      },
      contact: {
        Mobile: "  0967819889",
        Facebook: "  Napol H. Sriswan",
        Line: "  nhamn",
      },
      skill: {
        1: "JAVA",
        2: "PHP",
        3: "C++",
        4: "SQL",
        5: "English",
      },
    };
  },
  methods: {
    switchiconna() {
      this.tag_updown2 = true;
      this.tag_updown = false;
      this.tag_updown3 = false;
    },
    switchiconna2() {
      this.tag_updown2 = false;
      this.tag_updown = true;
      this.tag_updown3 = false;
    },
    switchiconna3() {
      this.tag_updown2 = false;
      this.tag_updown3 = true;
      this.tag_updown = false;
    },
    switchiconna4() {
      if (this.tag_updown4 == true) {
        this.tag_updown4 = false;
      } else {
        this.tag_updown4 = true;
      }
    },
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

  background-color: white;
  margin-right: 18%;
  border-radius: 30px;
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
.arr {
  font-size: 18px;
}
.arr_r {
  padding-left: 25%;
}
.end {
  margin-bottom: 5%;
}
</style>

