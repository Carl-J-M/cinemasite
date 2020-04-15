<template>
    <div class="page-container flex-container">
      <h1 class="splash-text flex-item" @click="picker">
        <span class="curve1">R</span>
        <span class="curve2">A</span>
        <span class="curve3">N</span>
        <span class="curve4">D</span>
        <span class="curve5">O</span>
        <span class="curve6">M</span>
        <span class="curve7">F</span>
        <span class="curve8">L</span>
        <span class="curve9">I</span>
        <span class="curve10">X</span>
      </h1>
      <div class="login-field flex-item"  id="random-movie">
        <button @click="picker">Choose!</button>
        <p id="chosenMovie">{{chosenName}}</p>
      </div>
      <div class="bottom-banner"></div>
    </div>
</template>

<script>
export default {
  name: 'LandingComponent',
  props: {
    msg: String
  },
  data(){
    return{
      list: [
      "Event Horizon",
      "Joker",
      "1917",
      "Dallas Buyers Club",
      "Toy Story 4",
      "Once Upon a Time in Hollywood",
      "The Fighter",
      "Flight",
      "Training Day",
      "The Report",
      "Fear and Loathing in Las Vegas",
      "Parasite",
      "Good fellas",
      "Lock, Stock & Two Smoking Barrels",
      "Friday",
      "Saving Private Ryan",
      "Whiplash",
      "The Big Lebowksi",
      "The Grand Budapest Hotel",
      "Stand by Me",
      "Mulan",
      "Kill Bill",
      "Emperors New Groove",
      "Zombieland 2",
      "Get Out",
      "What we do in the Shadows",
      "Annihilation",
      "Enemy",
      "Children of Men",
      "Chappie",
      "Hercules",
      "Hell Or High Water",
      "Waiting",
      "You Were Never Really Here",
      "John Wick"
  ],
      chosenName: ""
    }
  },
  methods: {
    picker: function(){
      var chosenNumber = Math.floor(Math.random() * this.list.length);
      this.chosenName = this.list[chosenNumber];
      console.log(this.chosenName);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.page-container {
  width: 100vw;
  height: 100vh;
  top: 0px;
  left: 0px;


  position: relative;
  background-image: url("../assets/KcGHmy.jpg");
  background-size: 110% 100%;

}
h1 span {
  background: #ED213A;  /* fallback for old browsers */
  background: -webkit-linear-gradient(to bottom, #93291E, #ED213A);  /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(to bottom, #93291E, #ED213A); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
  height: 600px;
  position: absolute;
  width: 50px;
  top: 0px;
  left: 0px;
  border: solid white 4px;
  transform-origin: bottom;
}
.curve1 { transform: rotate(6deg); }
.curve2 { transform: rotate(12deg); }
.curve3 { transform: rotate(18deg); }
.curve4 { transform: rotate(24deg); }
.curve5 { transform: rotate(30deg); }
.curve6 { transform: rotate(36deg); }
.curve7 { transform: rotate(42deg); }
.curve8 { transform: rotate(48deg); }
.curve9 { transform: rotate(54deg); }
.curve10 { transform: rotate(60deg); }

.flex-container {
      display: flex;
      justify-content: center;
      flex-direction: column;
      vertical-align: center;
}


.splash-text {
  font-size: 2em;
  color: white;
  margin-top: 10%;
  font-family: 'Bebas Neue', sans-serif;

}

.login-field {
  background-color: white;
  color: #ED213A;
  font-size: 36px;
  height: auto;
  margin: auto;
  padding: 8px;
  width: 100%;
  vertical-align: center;
  z-index: 1;
  font-family: 'Bebas Neue', sans-serif;
}

.bottom-banner {
  position: absolute;
  background-image: url("../assets/cinema.jpg");
  height: 40%;
  width: 100%;
  top: 60vh;
  background-size: 100% 180%;
  background-position: bottom;
  border-top: solid white 4px;
  filter: grayscale();


}
button {
  border: none;
  background: #EF5350;
  color: #fff;
  text-transform: uppercase;
  font-size: 1em;
  padding: 10px 20px;
  border-radius: 10px;
  cursor: pointer;
  box-shadow: 0 1px 5px rgba(68, 68, 68, 0.5);
}
.suggestion {
  color: white;
  font-size: 36px;
  position: absolute;
  top: 25%;
  left: 50%;
}
#chosenMovie {
  font-size: 50px;
  font-family: 'Bebas Neue', sans-serif;
}

</style>
