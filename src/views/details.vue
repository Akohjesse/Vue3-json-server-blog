<template>
 <div class="wrap">
      <div v-if="error">
          {{error}}
     </div>
  <div class="text_post" v-if="post">
         <h3>
            {{post.title}} 
         </h3>
         <div class="blog">
             <p>
                 {{post.body}}
             </p>
         </div>
  </div>
  <div v-else>
      Loading...
  </div>
 </div>
</template>

<script>
import getPost from '../composables/getPost'
export default {
   props: ['id'],

   setup(props){
     const {load, error , post} =   getPost(props.id)    

     load();

     return {post,error}
   }
}
</script>

<style lang="scss" scoped>
.wrap{
    width:80%;
    margin:0 auto;
}
.text_post{
    padding:10px;
    h3{
        color:orange;
        font-size:1.5em;
        text-align: center;
        margin:5px 0px;
    }
    .blog{
        p{
            line-height: 30px;
            padding: 10px;
        }
    }
}
</style>