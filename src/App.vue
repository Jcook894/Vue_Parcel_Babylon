<template>
  <div class="grid-container" id="app">
    <Canvas class="canvas"></Canvas>
    <ChatBox class="chat"></ChatBox>
     <Inventory class="inventory"></Inventory>
  </div>
</template>

<script>
import Inventory from './Inventory/Inventory.vue';
import ChatBox from './Chat_box/ChatBox.vue';
import Canvas from './Game_canvas/Canvas.vue';

export default {
  name: 'app',
  data () {
    return {
      msg: ' Lets get it!!!!!'
    }
  },
  components: {
    Inventory,
    ChatBox,
    Canvas
  }
}
</script>

<style lang="css">
  .grid-container {
    height: 100vh;
    display: grid;
    grid-gap: 5px;
  }

  .canvas{
    grid-column-start: 1;
    grid-row-start: 1;
    grid-column-end: 9;
    grid-row-end: 3;
  }

  .chat{
    background-color: grey;
    border-radius: 5px;
    grid-column-start: 1;
    grid-row-start: 3;
    grid-column-end: 9;
    grid-row-end: 7;
  }

  .inventory{
    background-color: grey;
    border-radius: 5px;
    grid-column-start: 9;
    grid-row-start: 1;
    grid-row-end: 7;
    grid-column-end: 10;
  }


  #app {
    color: #56b983;
    border: 1px solid black;
    max-height: 100%;
    overflow: hidden;
  }
</style>