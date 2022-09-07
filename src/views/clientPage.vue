<template>
    <div class="app" id="app">
        <div id="header">
            <H1 id="title">FOODIE</H1>
            <h3 id="Restaurants">Restaurants</h3>
            <h3 id="settings">Settings</h3>


        </div>
        <div id="main">
            <input type="text">
            <input type="password" name="undefined" id="test001">
            <button> login</button>
        </div>
        <div id="Footer">
            <p>foodie inc &copy;</p>
        </div>
    </div>
</template>

<script>
    import axios from "axios"
    import cookies from "vue_cookies"

    
    export default {
        methods:{
      create_cookie(){
        cookies.set("username", "password")
      }
    },
    
    mounted(){
        axios.get({ url:`https://innotechfoodie.ml/api/client`,
             'x-api-key': `tiSBwXqgUWRLQfxsygW`,
            
            
    
            }).then((response) => {
                return{
                    created_at:(String),
                    email: (String),
                    first_name:(String),
                    last_name: (String),
                    id:(Number),
                    img_url:(String),
                    username:(String)

                }
            }).catch((error) => {
                return ("ERROR 404 user not found")
            })
        }};
        axios.post({



        })
        
    
    
        
</script>

<style scoped>

</style>