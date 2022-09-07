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
    import cookies from "vue-cookies"
    export default {
        methods:{
      create_cookie(){
        cookies.set("username", "password")
      }
    },
    mounted(){
        axios.get({ url:` https://innotechfoodie.ml/api/restaurant`,
             'x-api-key': `tiSBwXqgUWRLQfxsygW`,
        
            
    
            }).then((response) => {
                return{
                    email: (string),
                    name: (string),
                    address: (string),
                    phone_number: (string),
                    bio: (string),
                    city: (string),
                    profile_url: (string),
                    banner_url: (string),
                    restaurant_id: (number)

                }
            }).catch((error) => {
                return ("ERROR 404 user not found")
            })
        }};
        
    
</script>

<style scoped>

</style>