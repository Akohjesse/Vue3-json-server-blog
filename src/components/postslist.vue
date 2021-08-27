<template>
    <div class="post-list">
           <div v-for="post in posts" :key="post.id">
               <Post :post="post" />
           </div>
    </div>
</template>

<script>
import Post from './posts.vue';
export default {
  props: ['posts'],
  components: { Post }
}
</script>

<style>
  .post-list{
    width:80%;
    margin: 50px auto;
    display: grid;
    grid-gap:20px;
    grid-template-columns: repeat(2, 1fr);
  }
</style>