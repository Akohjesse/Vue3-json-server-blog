<template>
 <div class="home">
   <div v-if="error">
     {{error}}
   </div>
   <div class="post_container" v-if="posts.length">
      <PostList class="PostList" :posts="posts" />
   </div>
   <div v-else>
     <h4>Loading....</h4>
   </div>
  
 </div>
</template>

<script>
import PostList  from "../components/postslist.vue";
import  getPosts from '../composables/getPosts'
export default { 
  name: 'Home',
  components: {PostList},
  setup(){

    const { posts, error, load } = getPosts();
    load();
     return { posts , error}
  }
}
</script>


<style lang="scss" scoped>
  .PostList{
    display: grid;
    grid-template-columns: repeat(2, 1fr);
  }
</style>