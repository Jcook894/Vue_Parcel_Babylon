<template>
  <div id="chat-box">
      <h2>Im where the Chat box is!!!</h2>
      <div class="messages"> Julian says: {{chat}}</div>
      <form>
        <input ref="my_input" class="chat-input" type="text" ></input>
        <button @click.prevent="onSubmit" type="submit">Submit</button>
      </form>
  </div>
</template>

<script>
export default {
  name: 'chat-box',
  data () {
    return {
      chat:''
    }
  },
  methods:{
    onSubmit(){
      this.chat = this.$refs.my_input.value;
    }
  }
}
</script>

<style>
  #chat-box{
    border: 1px solid black;
    overflow: hidden;
  }
  input{
    border-radius: 5px; 
    width: 85%;
  }
  .messages{
    max-height: 45%;
    max-width: 100%;
    overflow-y: scroll;
    border-radius: 5px; 
    padding: 10px;
    border: 1px solid black;
    background-color:  white;
  }
</style>
