<template>
  <div class="mycomponent">
    <h1 :id="myId">{{ msg }}</h1>
    <button class="mybtn" @click="cambiaColore">CAMBIA COLORE DEL TESTO</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      myId : "primo-id"
    }
  },
  methods : {
    cambiaColore() {
      if(this.myId == 'primo-id') {
        this.myId = 'secondo-id'
      }
      else {
        this.myId = 'primo-id'
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.mycomponent {
  border: 3px solid black;
  margin: 3px;
  padding: 10px;
}
#primo-id {
  color: red;
}
#secondo-id {
  color: blue;
}
.mybtn {
  background-color: black;
  color: white;
  border-radius: 20px;
  cursor: pointer;
  border: 2px white;
}
</style>
