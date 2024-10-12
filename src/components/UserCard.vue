<template>
    <div class="user-card">
        <div class="content">
            {{ user.content }}
            <div>
                Click here for user details:
                <RouterLink :to="href">Click me</RouterLink>
            </div>
        </div>
    </div>
    <slot>
    </slot>
</template>

<script>
    export default {
        props: {
            user: {
                type: Object
            }
        },
        computed: {
            href() {
                return "userDetail/"+this.$props.user.id
            }
        },
        data() {
            // return {
            //     username: this.props.user.username
            // }
        }
    }
</script>

<style scoped>
    .user-card {
        width: fit-content;
    }
</style>