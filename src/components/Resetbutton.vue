<template>
    <div>
        <button class="reset-btn" value="Reset Game">Reset Game</button>
    </div>
</template>

<script>
export default {
    name: "Resetbutton",
}
</script>

<style scoped>
.reset-btn {
  margin: auto;
  padding: 15px;
  text-align: center;
  text-transform: uppercase;
  transition: 0.5s;
  background-size: 200% auto;
  color: black;
 text-shadow: 0px 0px 10px rgba(0,0,0,0.3);
  border: none;
border-radius: 10px;
  width: 180px;
  min-height: 30px;
  font-size: 18px;
  background-image: url('../assets/board-bg.png');
  line-height: 20px;
  cursor: pointer;
}
.reset-btn:hover {
    transform: scale(1.15);
}
</style>