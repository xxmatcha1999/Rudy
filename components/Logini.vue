<template>
  <div>
    <img src="~/assets/logo_pic.png" width="300" height="300" />
    <div class="sign">
      <span class="sign__word " >SPACE SHOP</span>
    </div>
  </div>
</template>

<style>

html,
body {
	position: relative;
  margin: 0;
  height: 100%;
}


body {
  font-family: "Vibur", cursive;
  font-size: 1rem;
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  background-color: #141414;
}

/*-- Sign Styles --*/

.sign {
  min-height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.sign__word {
    font-size: 40px;
    text-align: center;
    line-height: 1;
    color: black;
    animation: neon .08s ease-in-out infinite alternate;
  }




@keyframes neon {
  from {
    text-shadow:
    0 0 6px rgba(202,228,225,0.92),
    0 0 30px rgba(202,228,225,0.34),
    0 0 12px rgba(30,132,242,0.52),
    0 0 21px rgba(30,132,242,0.92),
    0 0 34px rgba(30,132,242,0.78),
    0 0 54px rgba(30,132,242,0.92);
  }
  to {
    text-shadow:
    0 0 6px rgba(202,228,225,0.98),
    0 0 30px rgba(202,228,225,0.42),
    0 0 12px rgba(30,132,242,0.58),
    0 0 22px rgba(30,132,242,0.84),
    0 0 38px rgba(30,132,242,0.88),
    0 0 60px rgba(30,132,242,1);
  }
}


.NuxtLogo {
  animation: 1s appear;
  margin: auto;
}

@keyframes appear {
  0% {
    opacity: 0;
  }
}

</style>
