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

</style>