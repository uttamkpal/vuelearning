<template>
    <div class="cont">
        <h1>{{title}}</h1>
        <hr>
        <p v-if='num > 0'>Positive Number</p>
        <p v-else-if='num < 0'>Negative Number</p>
        <p v-else-if="num == 0" >Number is Zero</p>
        <p v-else>NON</p>
        <p v-show='show'> V-SHOW Derective</p>
        <template v-if="isDisplay">
            <div class="cont">
                <h2>Inner Template is Displayed</h2>
                <h2>List Rendering</h2>
                <p> <span v-for='item in list' :key ='item'>{{ item + ' ' }}  </span></p>
                <p> <span v-for='(item, index) in list' :key ='item'> {{index +1}} {{ item + ' ' }}  </span></p>
                <p v-for='(name, index) in nameOb' :key="index">{{index +1}} {{name.first +" "}}{{name.last}}</p>
                <div class="d-flex">
                    <div v-for='name in nameOb2' :key="name.first" class="contf">
                        <h2>{{name.first +" "}}{{name.last}}</h2>
                        <h4> Subject Code : <span v-for='code in name.subjectCode' :key='code'>{{code + " "}}</span></h4>
                    </div>
                </div>
                
            </div>
            
        </template>
    </div>
</template>


<script>
export default {
  name: 'conditionalRendering',
  data() {
    return {
     title:"Conditional Rendering",
     num :66,
     isDisplay : true,
     show : true,
     list: ['Uttam', 'Kumar', 'Pal'],
     nameOb:[
         { first:'Uttam', last:'Kumar'},
         { first:'udoy', last:'Kumar'},
         { first:'Rezaul', last:'Islam'},
     ],
     nameOb2:[
         { first:'Uttam', last:'Kumar', subjectCode: [4101,4102,4103]},
         { first:'udoy', last:'Kumar', subjectCode: [3101,3102,3103]},
         { first:'Rezaul', last:'Islam', subjectCode: [4101,4102,4103]},
     ],
    }
  },
}
</script>

<style scoped>

div.cont {
    width: 60%;
    margin: 0 auto;
    text-align: center;
    border:2px solid rgb(37, 58, 37);
    padding: 30px 10px;
}
.d-flex{
    display: flex;
}
</style>
