<template>
    <div>
        <div>
            <nav class="navbar">
                <div class="logo">
                    <h1>RoBlog</h1>
                </div>
                <div class="menu">
                    <h3>Home</h3>
                    <h3>Blogs</h3>
                    <h3>Login</h3>
                </div>
            </nav>
        </div>
    </div>

</template>

<script>
export default {
    name: 'Navbar',
    data() {
        return {
            msg: 'Welcome to Your Vue.js App'
        }
    }
}
</script>

<style>
.navbar {
    text-align: center;
    margin-top: -10px;
    color: #fff;
}
.logo {
    float: left;
    font: 1em sans-serif;
    margin-top: -1rem;
}
.menu {
    display: flex;
    justify-content: center;
    align-items: center;
    float: right;
}
.menu h3 {
    margin: 10px;
}
</style>