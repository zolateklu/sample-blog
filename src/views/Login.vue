<template>
    <div class="login-container">
        <div class="login-form">
            <div class="login-form-header">
                <h1>Login</h1>
            </div>
            <div class="login-form-body">
                <div class="login-form-input">
                    <label for="email" style="margin-right:2.5rem">Email</label>
                    <input type="email" id="email" name="email" placeholder="Email" v-model="email">
                </div>
                <div class="login-form-input">
                    <label for="password" style="margin-right:1rem">Password</label>
                    <input type="password" id="password" name="password" placeholder="Password" v-model="password">
                </div>
                <div class="login-form-link">
                    <a href="#">Forgot Password?</a>
                    <a href="register">Create Account</a>
                </div>
                <div class="login-form-button">
                    <button class="login-form-button" @click="login">Login</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Login',
    data(){
        return {
            email: '',
            password: ''
        }
    },
    methods:{
        login(){
            fetch('http://localhost:8000/api/user/login', {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json'
                },
                body: JSON.stringify({
                    email: this.email,
                    password: this.password
                })

            })
            .then(response => response.json())
            .then(res => {
                this.$router.push('/posts')
            })
            .catch(err => {
                console.log(err)
            })
        },
    }
}
</script>

<style>
.login-container {
    width: 100%;
    height: 30.7rem;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #D9D9D9;
    opacity: .9;
    margin-top: 3.1rem;
}
.login-form{
    width: 24rem;
    height: 24rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background-color: #CBCBCB;
}
.login-form-input{
    width: 100%;
    height: 2rem;
    margin: 1rem;
    text-align: left;
}
#email{
    margin-left: .2rem;
}
a{
    margin-left: 2rem;
}
.login-form-button{
    margin: 1rem;
    text-align: center;
}
</style>