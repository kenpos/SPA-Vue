<template>
<div>
    <h3>Home</h3>
    <button @click="toUsers">Usersのページへ移動</button>
</div>
</template>

<script>
    export default{
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