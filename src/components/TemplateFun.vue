<template>
    <div>
        <button @click=toggle_TF>CLICK ME</button>
        <div v-if="is_true == true" class="TemplateFun">
        
            <h1>{{ blog_title }}</h1>
            <p>{{ blog_content }}</p>
            <img :src="require(`@/assets/${blog_img_ulr}`)" > 
        </div>
    </div>
    
    
  </template>
  
  <script>
  export default {
        data(){
            return {
                blog_content:"test content",
                blog_title: "blog",
                blog_img_ulr: "logo.png",
                is_true : false
            }
        },
        methods:{
            toggle_TF(){
                this.is_true = !this.is_true;
                console.log(this.is_true);
            }
        }

  }
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped>
  
  </style>