<template>
    <div class="TemplateFun">
        <h1>{{ blog_title }}</h1>
        <p>{{ blog_content }}</p>
        <img :src="require(`@/assets/${blog_img_ulr}`)"/>
    </div>
  </template>
  
  <script>
  export default {
        data(){
            return {
                blog_content:"test content",
                blog_title: "blog",
                blog_img_ulr: "logo.png"
            }
        }

  }
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped>
  
  </style>