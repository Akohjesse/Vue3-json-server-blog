<template>
<nav>
    <ul>
        <router-link style="text-decoration:none" to="/" >Home</router-link>
        <li>
            <a href="https://akohjesse.com">Jesse</a>
        </li>
        <li>
            <a href="https://github.com">
             Github
            </a>
        </li>
    </ul>
</nav>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style lang="scss" scoped>
  nav{
      padding:10px 5px;
     ul{
          display: flex;
          flex-direction: row;
          justify-content: space-evenly;
         
          li{
                list-style-type: none;
               a{
                   text-decoration: none;
                
               }
          }
     }
  }
</style>