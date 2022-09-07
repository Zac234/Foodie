<template>
  <div id="app">
    <router-view/>

  </div>
  
</template>


<script>
  import axios from 'axios'
  import cookies from vue-cookies
  import clientPageVue from './views/clientPage.vue';
  import restaurantsPageVue from './views/restaurantsPage.vue';
  import menu from './views/menu.vue'
  export default{
    methods:{
      create_cookie(){
        cookies.set("username", "password")
      }
    },

    mounted(){
        axios.get({ url:`https://innotechfoodie.ml/api/client`,
             'x-api-key': `tiSBwXqgUWRLQfxsygW`
    
            }).then((response) => {
                console.log("successful test")
            }).catch((error) => {
                console.log("ERROR")
            })
        }};
        clientPageVue
        restaurantsPageVue
        menu    
    
  
</script>

<style>

</style>
