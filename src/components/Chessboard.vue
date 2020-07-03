<template>
    <div class="chessboard">
      <div class="boardborder"></div>

      <div class="point1"></div>
      <div class="point2"></div>
      <div class="point3"></div>
      <div class="point4"></div>
      <div class="point5"></div>

      <div class="edgecontainer-top">
        <div class="edgetile" v-for="(item,index) in edgeros" :key="index">
          <div class="lefttile"></div>
          <div class="righttile"></div>
        </div>
      </div>
      
      <div class="edgecontainer-bottom">
        <div class="edgetile" v-for="(item,index) in edgeros" :key="index">
          <div class="lefttile"></div>
          <div class="righttile"></div>
        </div>
      </div>

      <div class="edgecontainer-left">
        <div class="edgetile" v-for="(item,index) in edgeros" :key="index">
          <div class="lefttile"></div>
          <div class="righttile"></div>
        </div>
      </div>

      <div class="edgecontainer-right">
        <div class="edgetile" v-for="(item,index) in edgeros" :key="index">
          <div class="lefttile"></div>
          <div class="righttile"></div>
        </div>
      </div>

    <div class="centercontainer">
      <div class="rowcontainer" v-for="(item,index) in ros" :key="index">
        <Square v-for="(item,index) in cols" :key="index" ></Square>
      </div>
    </div>

    <Timer class="chesstimer"></Timer>

<div class="button-container">
    <Undobutton class="btn undobutton"></Undobutton>
    <Resetbutton class="btn Resetbutton"></Resetbutton>
</div>


    </div>
</template>

<script>
import Square from './Square';
import Timer from './Timer';
import Resetbutton from './Resetbutton';
import Undobutton from './Undobutton';

let model = {
  rows: 12,
  cols: ['A','B','C','D','E','F','G','H','i','j','K','L','M'],
  columns: 12,
  ros: [1,2,3,4,5,6,7,8,9,10,11,12,13],
  edgeros: [1,2,3,4,5,6,7,8,9,10,11,12,13,14],
  // v-for part reference:  
  //   Author: KiraYo4kage
  //   Source: https://github.com/KiraYo4kage/vue-gomoku/blob/master/vue-gomoku/src/components/Play.vue
  //   Date accessed: 27 Jun 2020
}

export default {
  name: 'Chessboard',
  components: {
    Square,
    Timer,
    Resetbutton,
    Undobutton,
  },
    data() {
    return model;
  },
}
</script>

<style scoped>
.button-container {
  position: fixed;
  right: 200px;
  bottom: 375px;
}
.btn {
  margin-top: 33px;
}
.chesstimer {
    position: fixed;
    right: 210px;
    font-size: 4em;
    color: whitesmoke;
}
.point1 {
  width: 11px;
  height: 11px;
  border-radius: 11px;
  top: 384px;
  left: 384px;
  background: black;
  position: absolute;
}
.point2 {
  width: 11px;
  height: 11px;
  border-radius: 11px;
  top: 180px;
  left: 180px;
  background: black;
  position: absolute;
}
.point3 {
  width: 11px;
  height: 11px;
  border-radius: 11px;
  top: 180px;
  left: 588px;
  background: black;
  position: absolute;
}
.point4 {
  width: 11px;
  height: 11px;
  border-radius: 11px;
  top: 588px;
  left: 588px;
  background: black;
  position: absolute;
}
.point5 {
  width: 11px;
  height: 11px;
  border-radius: 11px;
  top: 588px;
  left: 180px;
  background: black;
  position: absolute;
}
.boardborder {
  border: 4px solid black;
  position: absolute;
  width: 714.5px;
  height: 714.5px;
  top: 28.5px;
  left: 29px;
}
.chessboard {
  width: 780px;
  height: 780px;
  margin: 1em auto;
  background:url("../assets/board-bg.png");
  background-size: cover;
  border: 2px solid black;
  position: relative;
}
.centercontainer {
  width: 663px;
  position: absolute;
  left: 58.5px;
  top: 58.5px;
  right: 58.5px;
  bottom: 58.5px;
}
.edgecontainer-left {
  flex: 1;
  display: flex;
  transform: translate(-344.5px, 343.5px) rotate(-90deg);
}
.edgecontainer-right {
  flex: 1;
  display: flex;
  transform: translate(345.5px, 385.5px) rotate(90deg);
}
.edgecontainer-bottom {
  flex: 1;
  display: flex;
  transform: translate(33px, 722px) rotate(180deg);
  position: absolute;
}
.edgecontainer-top {
  flex: 1;
  display: flex;
  position: absolute;
  top: 32px;
  left: 33.5px;
}
.rowcontainer {
  flex: 1;
  display: flex;
}
  .edgetile {
    position: relative;
    width: 51px;
    height: 25px;
  }
  .lefttile {
  position: absolute;
  width: 25px;
  height: 25px;
  top: 0;
  left: 0;
  /* border-left: 1px solid black; */
  border-top: 1px solid black;
  }
  .righttile {
  position: absolute;
  width: 25px;
  height: 25px;
  top: 0;
  right: 0;
  border-right: 1px solid black;
  border-top: 1px solid black;
  }
</style>