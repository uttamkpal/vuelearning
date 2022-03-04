<template>
    <div class="bind">
        <h1>Bind Execise</h1>
        <hr>
        <h2>Hello {{ parson }}</h2>
        <h2>{{getting}} {{ parson }}</h2>
        <p v-bind:class='bind'>Lorem ipsum dolor sit amet,<span v-text='parson'></span> consectetur adipisicing elit.
             Ea soluta debitis quis beatae amet explicabo odit neque quam aliquam iusto.</p>
        <div v-html="html"></div>
        
        <div :class="classvar">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. 
            Temporibus cumque quae aperiam debitis alias quisquam dignissimos neque, laudantium, hic
             nostrum reprehenderit minus delectus ducimus? Doloremque dolorum quam alias 
             totam consectetur.
        </div>
    </div>
</template>
<script>

export default ({
    name: 'bindData',
    data() {
        return{
            parson: 'UTTAM KUMAR PAL',
            getting : 'Hello MR.',
            bind:'bind',
            html: "<h1>HTML</h1>",
            classvar:['active', 'fontchange', 'bind'],
        }
    },
})
</script>
<style scoped>
h2{
    color:green;
}
.bind  {
    width: 60%;
    margin: 0 auto;
    text-align: center;
    border:2px solid green;
    padding: 30px 10px;
}
.active{
    color:#3f3f3f
}
.fontchange{
    font-size: 36px;
    font-weight: 700;

}
</style>
