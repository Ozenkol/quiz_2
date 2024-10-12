<template>
    <div class="user-details">
        Current user id: {{ $route.params.id }}
        <form>
            Change username: 
            <input type="text">
        </form>
        <div class="detail">
            {{ user.name }}
            {{ user.username }}
        </div>
    </div>
</template>

<script>
    export default {
        props: {

        },
        data() {
            return {
                user: fetch('https://jsonplaceholder.typicode.com/users/'+ this.$route.params.id)
                    .then(response => response.json())
                    .then(json => console.log(json))
            }
        },
        
    }
</script>

<style scoped>
    .user-card {
        width: fit-content;
        height: 2em;
    }
</style>