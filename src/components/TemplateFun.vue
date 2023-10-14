<template>
    <div>
        <button @click=toggle_TF>CLICK ME</button>
        
        <div v-if="is_true == true" class="TemplateFun">
            <article v-for="(post, index) in posts" :key="index">
                <p>{{ post[`blog_title`] }}</p>
                <p>{{ post[`blog_content`] }}</p>
                <img :src="require(`@/assets/${post.blog_img_ulr}`)" >
            </article>
            <!-- <img :src="require(`@/assets/${post.blog_img_ulr}`)" >  -->
        </div>
    
    </div>
    
    
  </template>
  
  <script>
  export default {
        data(){
            return {
                posts:[
                {
                    blog_content:"test content",
                    blog_title: "blog",
                    blog_img_ulr: "logo.png",
                },
                {
                    blog_content:"more test content",
                    blog_title:"another test",
                    blog_img_ulr:"logo.png",
                },
                {
                    blog_content:"yet more test content",
                    blog_title:"yet another test",
                    blog_img_ulr:"logo.png",
                
                }
                ],
                is_true:false
                
                
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