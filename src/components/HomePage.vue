<template>
    <div class="flex-box">
        <div class="user" v-for="user in userList">
            <UserCard :user="user">
                <button>Edit</button>
            </UserCard>
        </div>
    </div>
</template>

<script>
import UserCard from './UserCard.vue';
export default {
    name: 'HomePage',
    components: {
        UserCard
    },
    data() {
        return {
            userList: [
                {id: 1, username:"Alex Johnson", content: "Content 1"},
                {id: 2, username:"Alex Johnson", content: "Content 2"},
                {id: 3, username:"Alex Johnson", content: "Content 3"},
                {id: 4, username:"Alex Johnson", content: "Content 4"},
                {id: 5, username:"Alex Johnson", content: "Content 5"},
                {id: 6, username:"Alex Johnson", content: "Content 6"},
            ]
        }
    }
}

</script>

<style scoped>
    .flex-box {
        display: flex;
        flex-direction: column;
    }
    .user {
        border: solid;
        border-radius: 5px;
        padding: 5px 5px 5px 5px;
        width: fit-content;
        margin: 10px 10px 10px 10px;
    }
</style>