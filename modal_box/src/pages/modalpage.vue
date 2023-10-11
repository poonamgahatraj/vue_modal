<template>
    <h2>Modal Example</h2>


<button @click="showmodal">Open Modal</button>

<div class="modal" v-if="showmodal_content">
    <div class="modal-content">
   
        <p>Some text in the Modal..</p>
        <button @click="closemodal"  style="border: none;
    background: white;
    color: grey;">X</button>
    </div>
</div>



</template>

<script>
export default{
    data(){
        return{
            showmodal_content : false
        }
    },

    methods:{
        showmodal(){
            this.showmodal_content=!this.showmodal_content
        },

        closemodal(){
            this.showmodal_content=false
        }
    }
}
</script>

<style>
.modal-content{
    display: flex;
    justify-content: space-between;
   
    width: 70%;
    align-content: center;
    align-items: center;
    margin: auto;
    height: 70px;
    background:white;


}

.modal{
    position: fixed;
  z-index: 1; 
  padding-top: 100px; 
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  
  background-color: rgb(0,0,0);
  background-color: rgba(0,0,0,0.4); 
}
</style>