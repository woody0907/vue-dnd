<template>
  <main id="app" class="flexbox">

    <Board id="board1">
        <Card id="card1" draggable="true">this is card1</Card>
    </Board>
    <Board id="board2">
      <Card id="card2" draggable="true">this is card2</Card>
    </Board>
  </main>
</template>

<script>

import Board from './components/Board'
import Card from './components/Card'
export default {
  name: 'App',
  components: {
    Board,
    Card
  },

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.flexbox{
  display:flex;
  width:500px;
  height: 500px;
  justify-content: space-between;
  overflow: hidden;
  margin: 0 auto;
  padding:15px;
}
.flexbox .board {
    max-width: 200px;
    width: 100%;
    background-color: black;
    display: flex;
    flex-direction: column;
    padding: 15px;

}

.flexbox .board .card {
   background-color: antiquewhite;
   padding: 15px 25px;
   cursor: pointer;
   margin-bottom: 15px;

}
</style>
