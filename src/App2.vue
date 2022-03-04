<template>
<div>
    <h2>UTTAM Kumar Pal form app2</h2>
    <p v-bind ="objectAttrs">Object attributes</p>
    <div :class="flex">
        <div :class='box'>Box</div>
        <div :class='`${box} ${red}`'>Box</div>
        <div v-bind='attrsForBox'>Box</div>
    </div>
</div>
  
  
</template>

<script>
export default {
    name:'App2A',
    data() {
        return {
            objectAttrs:{
                id:'P',
                class: 'red'
            },
            attrsForBox:{
                class:'box'
            }, 
            box:'box',
            red:'red',
            flex:'flex',


        }
    },
}
</script>

<style>
#app2 {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
#P{
    border: 1px solid #2c3e50;
    padding: 20px 0;
}
.flex{
    display: flex;
}
.box{
    height: 150px;
    width: 150px;
    margin: 0 auto;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: green;
    color: white;
}
.red{
    background-color: red;
}
</style>