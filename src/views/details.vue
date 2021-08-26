<template>
 <div class="wrap">
      <div v-if="error">
    {{error}}
  </div>
  <div v-if="post">
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

<style>

</style>