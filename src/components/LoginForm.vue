<template>
    <div class="container form">
        <div class="container__email">
            <label for="form__email" class="label__email">Email</label>
            <input type="email" id="form__email" v-model="email">
        </div>
        <div class="container__password">
            <label for="form__password" class="label__password">Password</label>
            <input type="password" id="form__password" v-model="password">
        </div>
        <button @click="login">Login</button>
    </div>
</template>

<script>
export default {
    name: "LoginForm",
    data: () => ({
        email: '',
        password: ''
    }),
    methods: {
            login () {
                this.$emit('login', {
                    email: this.email,
                    password: this.password
                })
            }
    }
}
</script>

<style scoped>

</style>