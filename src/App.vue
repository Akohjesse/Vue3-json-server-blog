<template>
   <div class="main">
       <Header class="header"/>
      <router-view/>
   </div>
</template>

<script>
import Header  from "./components/header.vue";
export default {
   name: 'App',
   components: { Header }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Poppins&display=swap');
 *{
   box-sizing: border-box;
   padding:0px;
   font-family: 'Poppins', sans-serif;
   margin:0px;
 }
 .header{
    margin-bottom: 50px;
    padding:5px 0px;
 }
 .main{
  width:90%;
  margin:0 auto;
 }
</style>
