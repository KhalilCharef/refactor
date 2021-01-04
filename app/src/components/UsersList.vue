<template>
    <div className="container">
    <table border="1" width="80%" style="border-collapse : collapse">
    <tr>
        <th>Username</th>
        <th>Name</th>
        <th>Email</th>
    </tr>
    <tr v-for="user in users" v-bind:key="user">
        <td>{{user.username}}</td>
        <td>{{user.name}}</td>
        <td>{{user.email}}</td>
    </tr>
    </table>
    </div>
</template>
<script>
export default {
name: "UsersList",
data () {
    return {
        users: {}
    }
},
methods: {
    getUsers: function () {
        axios.get('')
        .then(response => {this.users = response.data})
    }
}   
}
</script>
<style scoped>

</style>
