<template>
    <div>
        <LoginForm @login="onLogin"/>
        <h3>{{email}} {{password}}</h3>
        <User v-for="user in users"
              :key="user.id"
              :name="user.name"
              :description="user.description"
              :isActive="user.isActive"
        />
    </div>
</template>

<script>
import User from "@/components/User";
import LoginForm from "@/components/LoginForm";
export default {
    name: "index",
    data: () => ({
        email: '',
        password: '',
        users: [
            {
                id: 1,
                name: 'Ivan',
                description: 'description',
                isActive: false
            }
        ]
    }),
    methods: {
        onLogin (data) {
            this.email = data.email;
            this.password = data.password;
            console.log('child component sail login', data)
        }
    },
    components: {User, LoginForm}
}
</script>

<style scoped>

</style>