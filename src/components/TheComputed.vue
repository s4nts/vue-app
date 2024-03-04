<template>
    <div>
        <h1>{{ user.first_name }} {{ user.last_name }}</h1>
    </div>
</template>

<script>
export default {
    name: "App",
    data() {
        return {
            user: {
                first_name: 'Jon', 
                last_name: 'Snow',
            }
        }
    },
    computed: {
        fullName() {
            this.
        }

    }
}
</script>

<style>
</style>