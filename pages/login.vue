<template>
  <div class="">
    <div class="container">
      <div class="bg">
          <b-row>
    <b-col><Logini/></b-col>
    <b-col><div>
          <h1 style="color: black"  class="fonts">Login or <a href="login">Sign Up</a></h1>
          <b-row class="start">
            <b-col class="text-center">
              <div class="">
                <a
                  href="#"
                  class="btn btn-primary btn-block btn-lg active"
                  role="button"
                  aria-pressed="true"
                  >Facebook</a
                >
              </div>
            </b-col>
            <b-col class="text-center">
              <div class="">
                <a
                  href="#"
                  class="btn btn-danger btn-block btn-lg active bg_g"
                  role="button"
                  aria-pressed="true"
                  >Google</a
                >
              </div>
            </b-col>
          </b-row>
          <br />
          <form>
            <div class="form-group">
              <input
                type="email"
                v-model="em"
                class="form-control"
                placeholder="Enter email"
              />
            </div>
            <div class="form-group">
              <input
                type="password"
                v-model="pass"
                class="form-control"
                id="exampleInputPassword1"
                placeholder="Password"
              />
            </div>
            <button type="button" @click="checkemail()" class="btn btn-primary">
              Login
            </button>
          </form>
        </div></b-col>
  </b-row>

        
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      email: "admin@gmail.com",
      password: "1234",
      xx: "",
      el: "#index_shop",
    };
  },
  methods: {
    checkemail() {
      if (this.em == this.email) {
        if (this.pass == this.password) {
          alert("Login");
          window.location = "index_shop";
        } else {
          alert("Wrong Email or Password");
        }
      } else {
        alert("y");
      }
    },
  },
};
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
.bg {
  background-color: white;
  border-radius: 10%;
  padding: 4% 6% 4% 6%;
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

.links {
  padding-top: 15px;
}
body {
  background-image: url("assets/bg2.jpg");
  background-color: #cccccc;
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-size: 100% 100%;
}
.fonts{
    font-size: 35px;
}
</style>
