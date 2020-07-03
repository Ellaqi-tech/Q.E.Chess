<template>
  <div id="app">
    <img alt="Chess logo" src="./assets/logo.png">
    <h1>Wuziqi Game</h1>
    <Chessboard msg="Wuziqi Game"/>

    <div class="chessbowlContainer">
      <div class="sideChessman sideblack chessglow"></div>
      <div class="sideChessman sidewhite"></div>
    </div>

    <div class="game-intro">
      <span class="closebtn" onclick="this.parentElement.style.display='none';">&times;</span> 
      <h2>Game Rules</h2>
      <p class="gamerule">Black chess move first. White and black chess take turns. One side of the five pieces of the same colour connected horizontally and diagonally wins. 
      The traditional strategy is that black chess is mainly offensive, and white pieces are mostly of defence, but unexpected strategy always wins. <br>
      Have fun!
      </p>
    </div>

  </div>
</template>

<script>
import Chessboard from './components/Chessboard.vue'

export default {
  name: 'App',
  components: {
    Chessboard,
  }
}
</script>

<style>
h2 {
  font-size: 3em;
  text-shadow: 1px 1px 5px black;
  padding: 10px;
}
.gamerule {
  font-size: 2em;
  text-align: left;
  padding: 5px 60px;
  text-shadow: 1px 1px 5px black;
}
.game-intro {
  padding: 50px;
  background: url("./assets/notebg.jpg");
  background-size: cover;
  color: white;
  position: fixed;
  top: 160px;
  left: 250px;
  right: 250px;
  bottom: 200px;
  box-shadow: 6px 6px 40px black;
}

.closebtn {
  margin-right: 20px;
  color:rgb(163, 59, 59);
  font-weight: bold;
  float: right;
  font-size: 50px;
  line-height: 20px;
  cursor: pointer;
  transition: 0.3s;
}

.closebtn:hover {
  color: black;
}

html {
  background: url("./assets/bg.jpg") top center;
  background-size: cover;
  box-sizing: border-box;
  overflow: hidden;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 20px;
}
h1 {
  color: white;
}
.chessbowl {
  width: 150px;
}
.chessbowlContainer {
  position: fixed;
  top: 35%;
  left: 10%;
}
.sideChessman {
  width: 80px;
  height: 80px;
  border-radius: 80px;
  margin: 8% 8%;
  z-index: 99;
  box-shadow: 3px 3px 6px black;
  position: relative;
}
.sidewhite {
  margin-top: 15em;
  background: radial-gradient(circle at 65% 15%, rgb(240, 239, 239) 3px, rgb(227, 228, 228) 3%, rgb(252, 252, 252) 60%, rgb(80, 79, 79) 100%);  
}
.sideblack {
 background: radial-gradient(circle at 65% 15%, rgb(128, 127, 127) 3px, rgb(116, 117, 117) 3%, black 60%, rgb(54, 54, 54) 100%); 
}

.chessglow {
 box-shadow: 0px 0px 30px 10px snow; 
 animation: chessglow 1s infinite alternate;
}
@keyframes chessglow {
  0% {box-shadow: 0px 0px 30px 5px snow;}
  100% {box-shadow: 0px 0px 50px 20px snow;}
}

/* .black::after {
position: absolute;
top: 0;
left: 0;
right: 0;
bottom: 0;
box-shadow: 120px 80px 40px 20px snow;
} */

</style>
