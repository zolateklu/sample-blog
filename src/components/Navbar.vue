<template>
    <div>
        <nav :class="{change_color: scrollPosition > 50}" class="navbar" v-bind:style="$route.path === '/blogs' ? 'background-color: #adadad;height: 3rem;margin-right: -.6rem' : $route.path === '/login'? 'background-color: #c4c4c4;height: 3rem;margin-right:-.6rem;margin-left:-.5rem;margin-bottom:-2rem;margin-top:-.16rem': $route.path === '/register'? 'background-color: #c4c4c4;height: 3rem;margin-right:-.6rem;margin-left:-.5rem;margin-bottom:-2rem;margin-top:-.16rem': $route.path ==='/'? 'margin-top:-.2rem;margin-right:-.5rem': '' ">
                <div class="logo">
                    <h1>RoBlog</h1>
                </div>
                <div v-if="$route.path === '/blogs'" class="search">
                    <svg xmlns="http://www.w3.org/2000/svg" style="display: none;">

                    <symbol id="icon-search" xmlns="http://www.w3.org/2000/svg" viewBox="4330.5 149.786 19.571 19.571">
                            <path fill="currentColor" d="M4343.86 158.14a5 5 0 0 1-5 5 5 5 0 0 1-5-5 5 5 0 0 1 5-5 5 5 0 0 1 5 5zm5.7 9.3a1.44 1.44 0 0 0-.4-1l-3.83-3.84a7.84 7.84 0 0 0 1.38-4.45 7.85 7.85 0 0 0-7.84-7.86 7.85 7.85 0 0 0-7.86 7.84 7.85 7.85 0 0 0 7.86 7.86 7.84 7.84 0 0 0 4.45-1.38l3.84 3.8a1.4 1.4 0 0 0 1 .44 1.44 1.44 0 0 0 1.43-1.43z"/>
                        </symbol>

                    </svg>

                    <div class="c-search-box">
                    <label class="c-search-box__label">
                                        <span class="is-visually-hidden">Search term</span>
                                        <input id="c-search-box__input--power" type="text" class="c-search-box__input" placeholder="Enter search terms…" />
                                        <button>
                                            <svg class="o-icon c-search-box__icon">
                                                <use xlink:href="#icon-search" />
                                            </svg>
                                        </button>
                                        <input type="submit" value="search" class="is-visually-hidden" />
                                    </label>
                    </div>
                </div>
                <div class="menu">
                    <button @click="home">Home</button>
                    <button @click="blogs">Blogs</button>
                    <button @click="login">Login</button>
                </div>
            </nav>
        </div>

</template>

<script>
export default {
    name: 'Navbar',
    data(){
        return{
            scrollPosition: 0,
        }},
    methods: {
        updateScroll(){
            this.scrollPosition = window.scrollY
            },
        home() {
            this.$router.push('/')
        },
        blogs() {
            this.$router.push('/blogs')
        },
        login() {
            this.$router.push('/login')
        }
    },
    mounted(){
            window.addEventListener('scroll', this.updateScroll)
        },
}
</script>

<style>
nav {
    width: 100%;
    height: 3rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    opacity: .9;
    position: fixed;
}
.change_color {
       background-color: lightgrey;
       opacity: 1;
   }
.navbar {
    text-align: center;
    color: #fff;
    margin-top: -10px;
}
.logo {
    float: left;
    font: 1em sans-serif;
    margin-top: -1rem;
    margin-left: 4rem;
}
.search{
    float: center;
    width: 30rem;
    height: 2rem;
    margin-top: -6.7rem;
    margin-left: 23rem;
    }
.is-visually-hidden {
    position: absolute;
    overflow: hidden;
    clip: rect(0, 0, 0, 0);
    width: 1px;
    height: 1px;
    margin: -1px;
    padding: 0;
    border: 0;
}

.o-icon {
    width: 1rem;
    height: 1rem;
}

button {
    font-family: sans-serif;
    font-weight: normal;
    line-height: 1;
    display: inline-block;
    transition: background-color .2s ease-in-out, color .2s ease-in-out;
    max-width: 300px;
    padding: .75em 1.5em;
    cursor: pointer;
    text-align: center;
    vertical-align: middle;
    color: #fff;
    border: 1;
    background-color: #333333;
    
}
button:hover{
    outline: 0;
    background-color: rgb(196, 51, 26);
} 
button:focus{
    box-shadow: 0 0 15px rgba(rgb(228, 88, 63), .5);
    outline: 0;
    background-color: darken(tomato, 10%);
}
button:active{
    color: tomato;
    background-color: #fff;
    box-shadow: 0 0 15px rgba(tomato, .5);
}
.c-search-box {
    max-width: 20rem;
    margin: 0 auto;
    padding: 3rem 0 2.5rem;
    text-align: center;
    height: 2rem;
}


.c-search-box__input {
    margin-bottom: 0;
    border: 1px solid #2e2e2e;
    padding: 1em;
    width: 100%;
}

.c-search-box__label {
    display: flex;
}

.c-search-box__icon {
    color: #fff;
}
.c-search-box__icon button:active{
    color: tomato;
}

.menu {
    display: flex;
    justify-content: center;
    align-items: center;
    float: right;
    margin-top: -1rem;
}
.menu button {
    border: none;
    margin: 10px;
    margin-right: 30px;
    color: #fff;
    font-size: 1.1rem;
    background: transparent;
    cursor: pointer;
}
.menu button:hover {
    background: rgb(196, 180, 180);
    color: #000;
}

</style>