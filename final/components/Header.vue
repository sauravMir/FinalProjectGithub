<template>
<div >
    <b-navbar style="background-color: grey; padding : 10px">
       <template slot="start">
            <b-navbar-item href="#">
                Home
            </b-navbar-item>
            <b-navbar-item href="#">
                Documentation
            </b-navbar-item>
        </template>
    

     <template slot="end">
        
    <b-navbar-item 
    tag="router-link" :to="routes.stockLink">
    Stocks 
    </b-navbar-item>

    <b-navbar-item 
    tag="router-link" :to="routes.stockLink">
    Stocks 
    </b-navbar-item>

    </template>
    </b-navbar>
</div> 
</template>


<script>
export default {
    data() {
        return {
            routes: {
                stockLink: "/stocks",
                portfolioLink: "/portfolio"
            }
        }
    },
}
</script>