<template>
    <div class="square">
      
      <div class="tile1"></div>
      <div class="tile2"></div>
      <div class="tile3"></div>
      <div class="tile4"></div>
      <Chessman v-on:click="showhidden()"></Chessman>
    </div>
</template>

<script>
import Chessman from './Chessman'


export default {
  name: 'Square',
  components: {Chessman},
  data: function() {
        return {
            //chessmanHidden: true,
            show: false,
        }
    },
    methods: {
        showhidden: function() {
            // if(this.chessmanHidden) {
            //     this.chessmanHidden = false;
            // } else {
            //     this.chessmanHidden = true;
            // }
            alert("works");
        }
    }
}
</script>

<style scoped>
.square {
   width: 51px;
   height: 51px;
   position: relative;
 }
 .tile1, .tile2, .tile3, .tile4 {
   z-index: 0;
 }
.tile1 {
  position: absolute;
  width: 25px;
  height: 25px;
  top: 0;
  left: 0;
  border-right: 1px solid black;
}
.tile2 {
  position: absolute;
  width: 25px;
  height: 25px;
  top: 0;
  right: 0;
  border-bottom: 1px solid black;
}
.tile3 {
  position: absolute;
  width: 25px;
  height: 25px;
  right: 0;
  bottom: 0;
  border-left: 1px solid black;
}
.tile4 {
  position: absolute;
  width: 25px;
  height: 25px;
  bottom: 0;
  left: 0;
  border-top: 1px solid black;
}
</style>
