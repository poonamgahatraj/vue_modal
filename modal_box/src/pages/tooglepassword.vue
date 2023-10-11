<template>
<p>Click the radio button to toggle between password visibility:</p>
<div class="form">
     Password:<br><br>
     <input :type="fieldType"><br><br>

     <input type="checkbox" @click="pw_visible" > Show password<br>
</div>


</template>

<script>
export default{
    data(){
        return{
            fieldType:'password'
        }
    },
    methods:{
        pw_visible(){

            console.log("check")
            if (this.fieldType == "password") {
            this.fieldType = "text";
        }
         else this.fieldType = "password";
}
        }
    
}

</script>

<style>
.form{
    
    padding: 10px;
    background: lightseagreen;
    width: 30%;
   
    margin: auto;
    border-radius: 10px;
}

</style>