<template>
       <div class="item">
               <router-link style="text-decoration: none;" :to="{name: 'Details', params: { id: post.id}}">
                   <h3>{{post.title}}</h3>
              </router-link>
               <p>{{snippet}}....</p>
                <div class="tags">
                     <span v-for="tag in post.tags" :key="tag">
               #{{ tag }} 
            </span>
                </div>
       </div>
</template>

<script>
import { computed } from "vue";
export default {
props: ['post'],
setup(props){
    const snippet = computed(()=>{
       return props.post.body.substring(0,100)
    })
    return { snippet }
    }
}
</script>

<style lang="scss" scoped>
.item{
    border-radius: 5px;
    padding:20px;
    height: 13em;
    h3{
        color:orange;
        text-decoration: none;
    }
    p{
        margin:5px 0px;
    }
   .tags{
       margin:20px 0px;
        span{
        background: rgb(97, 97, 97);
        padding:6px;
        border-radius: 9px;
        margin-right:5px;
        color: rgb(255, 255, 255);
    }
   }
}
</style>