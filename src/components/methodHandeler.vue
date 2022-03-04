<template>
  <div class="cont">
      <h1>{{title}}</h1><hr>
      <h2>Inline Expresion {{2+5+3}}</h2>
      <h2>Simple Function {{add()}}</h2>
      <h2>Method With Parameter {{sum(32,43,43)}}</h2>
      <h2>method with Param and this {{multiple(3)}}</h2>
      <h2>method with Param and this {{multiple(baseNum)}}</h2>
      <br>
      <h1>Event Handeling</h1><hr>
      <h2 :style="{'font-size' :'48px'}">{{count}}</h2>
      <div class="d-flex">
          <button v-on:click='count++'>Increment</button>
          <button v-on:click='count--'>Decrement</button>
          <button @click='increment'>Increment 4</button>
          <button @click='decrement'>Decrement 4</button>
          <button @mouseover='increment'>Hover</button>
          <button @mouseover='decrement'>Hover</button>
      </div>
      <div class="d-flex p-3">
          <button @mouseleave='increment' @mouseenter="decrement">mouseenter</button>
          <button @mouseleave='decrement' @mouseenter="increment">mouseleave</button>
          <button @keypress='increment' @keyup="decrement">keypress, up</button>
          <button @mousemove='decrement' @mouseup="increment">mouseMove Up</button>
      </div>
      
  </div>
</template>

<script>
export default {
name: 'methodHandeler',

data(){
    return{
        title:'Method Handeler ',
        baseNum: 10,
        count: 0,
        count2: 0,
    }
},
methods:{
    add(){
        return 4+5+92
    },
    sum(a,b,c){
        return a+b+c
    },
    multiple(num){
        return num* this.baseNum
    },
    increment(){
        this.count +=4
    },
    decrement(){
        this.count -=4
    }

}
}
</script>

<style>
div.cont {
    width: 60%;
    margin: 0 auto;
    text-align: center;
    border:2px solid rgb(37, 58, 37);
    padding: 30px 10px;
}
.d-flex{
    display: flex;
    justify-content: space-around;
}
button{
    padding: 10px 20px;
    background-color: rgb(172, 48, 48);
    color: #fff;
}
.p-3{
    padding: 2rem 0;
}
</style>