<template>
<div>
    <h3>Home</h3>
    <button @click="toUsers">Usersのページへ移動</button>
    <p>{{ doubleCount }}</p>
    <p>{{ tripleCount }}</p>
</div>
</template>

<script>
import {mapGetters} from "vuex"

    export default{
        computed: {
        ...mapGetters(["doubleCount","tripleCount"])
        },
        methods:{
            toUsers(){
                this.$router.push( { 
                    name : 'users-id-props', 
                    params: { id: 1 }
                } );
            }
        }
    };
</script>