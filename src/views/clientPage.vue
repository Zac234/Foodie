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
    </div>
</template>

<script>
    import axios from "axios"
    
    export default {
    mounted(){
        axios.get({ url:`https://innotechfoodie.ml/api/client`,
             'x-api-key': `tiSBwXqgUWRLQfxsygW`
    
            }).then((response) => {
                console.log("successful test")
            }).catch((error) => {
                console.log("ERROR")
            })
        }};
    
    
        
</script>

<style scoped>

</style>