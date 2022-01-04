<template>
    <div class="register-container">
        <div class="register-form">
            <h1>Register</h1>
            <form @submit.prevent="register">
            <div class="form-group">
                <label for="fname">First Name</label>
                <input type="text" name="fname" v-model="fname" class="form-control" id="fname" placeholder="Enter your first name">
            </div>
            <div class="form-group">
                <label for="lname">Last Name</label>
                <input type="text" name="lname" v-model="lname" class="form-control" id="lname" placeholder="Enter your last name">
            </div>
            <div class="form-group">
                <label for="register-email">Email</label>
                <input type="email" name="register-email" v-model="email" class="form-control" id="register-email" placeholder="Enter your email">
            </div>
            <div class="form-group">
                <label for="register-password">Password</label>
                <input type="password" name="register-password" v-model="password" class="form-control" id="register-password" placeholder="Enter your password">
            </div>
            <div class="form-group">
                <label for="password_confirmation">Confirm Password</label>
                <input type="password" name="password_confirmation" v-model="password_confirmation" class="form-control" id="password_confirmation" placeholder="Confirm your password">
            </div>
            <button type="submit" class="btn btn-primary">Register</button>
            <div class="form-login-login" style="margin-top: 1rem;">
                <p>Already have an account?<a href="login">Login</a></p>
            </div>
            </form>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Register',
    data(){
        return{
            fname: '',
            lname: '',
            email: '',
            password: '',
            password_confirmation: '',
        }
    },
    methods: {
        register() {
            this.$http.post('/api/register', {
                fname: this.fname,
                lname: this.lname,
                email: this.email,
                password: this.password,
                password_confirmation: this.password_confirmation
            }).then(response => {
                this.$router.push('/login')
            })
        },
    }
}
</script>

<style>
.register-container {
    width: 100%;
    height: 31.15rem;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #D9D9D9;
    opacity: .9;
}
.register-form{
    width: 30rem;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background-color: #CBCBCB;
}
.form-group{
    width: 100%;
    height: 2rem;
    margin: 1rem;
    text-align: left;
}
#fname{
    margin-left: 4.5rem;
}
#lname{
    margin-left: 4.6rem;
}
#register-email{
    margin-left: 6.9rem;
}
#register-password{
    margin-left: 5rem;
}
#password_confirmation{
    margin-left: 1.2rem;
}
.btn{
    margin-top: 1rem;
}

</style>