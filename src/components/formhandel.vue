<template>
  <div class="cont">
      <div class="showBox">
          <pre>
              {{JSON.stringify(formValue, null, 2)}}
          </pre>
      </div>
    <h1>Form Handel</h1>
    <hr>
    <form @submit.prevent="formSubmit">
        <div class="d-flex">
            <label for="name">Name : </label>
            <input id="name" type="text" v-model="formValue.name">
        </div>
        <div class="d-flex">
            <label for="profileSumary">Profile Summary : </label>
            <textarea rows='5' id="profileSumary" type="text" v-model="formValue.profileSumary"> </textarea>
        </div>
        <div class="d-flex">
            <label for="country">Country : </label>
            <select id="country" v-model="formValue.country">
                <option value='' >Select Your Country</option>
                <option value="Bnagladesh">Bangladesh</option>
                <option value="India">India</option>
                <option value="USA">USA</option>
            </select>
        </div>
        <div class="d-flex">
            <label for="job-location">Job-Location : </label>
            <select id="job-location" multiple v-model="formValue.jobLocation">
                <option value="Bnagladesh">Bangladesh</option>
                <option value="India">India</option>
                <option value="USA">USA</option>
            </select>
        </div>
        <div class="text-left py-2">
            <input type="checkbox" id="remotwork" v-model="formValue.remotWork" true-value='Yes' false-value='No'>
            <label for="remotwork">Open to Remot Work</label>
        </div>
        <h4 class="text-left">Skill Set</h4>
        <div class="d-flex">
            <div>
                <input name="skill" type="checkbox" id="HTML" value="HTML" v-model="formValue.skillset" >
                <label for="HTML">HTML</label>
            </div>
            <div>
                <input name="skill" type="checkbox" id="JavaScript" value="JavaScript" v-model="formValue.skillset" >
                <label for="JavaScript">JavaScript</label>
            </div>
            <div>
                <input name="skill" type="checkbox" id="Vue" value="Vue" v-model="formValue.skillset" >
                <label for="Vue">Vue</label>
            </div>
            <div>
                <input name="skill" type="checkbox" id="Laravel" value="Laravel" v-model="formValue.skillset" >
                <label for="Laravel">Laravel</label>
            </div>
            
        </div>
        <h4 class="text-left"> Years Of Experience </h4>
        <div class="d-flex">
            <div>
                <input type="radio" id="0-2" name="fav_language" value="0-2" v-model="formValue.yearsOfExperience">
                <label for="0-2">0-2</label>
            </div>
            <div>
                <input type="radio" id="3-5" name="fav_language" value="3-5" v-model="formValue.yearsOfExperience">
                <label for="3-5">3-5</label>
            </div>
            <div>
                <input type="radio" id="5-10" name="fav_language" value="5-10" v-model="formValue.yearsOfExperience">
                <label for="5-10">5-10</label>
            </div>
            <div>
                <input type="radio" id="10+" name="fav_language" value="10+" v-model="formValue.yearsOfExperience">
                <label for="10+">10+</label>
            </div>
        </div>
        <button @submit="formSubmit" type="submit">Submit</button>
    </form>
  </div>
</template>

<script>
export default {

name:'formHandel',
data(){
    return {
        formValue:{
            name: '',
            profileSumary: '',
            country: '',
            jobLocation:[],
            remotWork: "No",
            skillset: [],
            yearsOfExperience : ''

        },
    }
},
mwthods:{
    formSubmit(){
        console.log("Form Submited", this.formValue);
    }
}
}
</script>

<style>
.cont{
    width: 60%;
    margin: 0 auto;
    
    border:2px solid green;
    padding: 10px 15px;
}
.showBox{
    border: 3px solid #5d5a5a;
    text-align: left;
    font-size: 18px;
}
.d-flex{
    display: flex;
    justify-content: start;
    margin: 20px 5px;
    align-items: center;
}
label{
    padding: 0 10px;
    width: 20%;
    text-align: end;
}
input[type=text], select, textarea{
    padding: 5px 10px;
    border: 1px solid #5d5a5a;
    outline: none;
    width: 80%;
    font-size: 24px;
    border-radius: 10px;
}

input[type="checkbox"]{
background-color: rgb(195, 12, 12);
border: 5px solid #f00;

}
.text-left{
    text-align: left;
}
.py-2{
    padding: 10px 0;
}
</style>