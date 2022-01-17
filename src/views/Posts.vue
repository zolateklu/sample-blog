<template>
    <div class="post-container">
        <div class="post-content">
            <div class="post-content-title">
                <div class="post-content-title-title">
                    <h3>Title</h3>
                </div>
                <div class="post-content-title-input">
                    <input type="text" placeholder="Write the title of the blog" v-model="title">
                </div>
            </div>
             <div class="post-content-body">
                <div class="post-content-body-body">
                    <h3>Body</h3>
                </div>
                <div class="post-content-body-textarea">
                    <textarea v-model="body"></textarea>
                </div>
            </div>
            <div class="post-image">
                <input type="file" name="image" id="image" @change="onFileChange">
            </div>
            <div class="post-button">
                <button class="post-button-button" @click="blogPost">Post</button>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Posts',
    data() {
        return {
            post: {},
            title: '',
            body: '',
            image: '',
        }
    },
    methods: {
        onFileChange(e) {
            const file = e.target.files[0]
            this.post.image = file
        },
        blogPost() {
            fetch('http://localhost:8000/api/post/postBlog', {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json'
                },
                body: JSON.stringify({
                    title: this.title,
                    body: this.body,
                    image: this.image,
                })
            })
        }
    }
}
</script>

<style>
.post-container{
    width: 100%;
    height: 100%;
    background-color: #D9D9D9;
    display: flex;
    justify-content: center;
    align-items: center;
}
.post-content{
    width: 58%;
    height: 25rem;
    background-color: #CBCBCB;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin: 4.4rem;
}
.post-content-title{
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 2rem;
    text-align: left;
}
.post-content-title-title{
    width:10%;
    margin-left: 4.7rem;
}
.post-content-title-input{
    width:90%;
    height: 2rem;
    margin-left: -.5rem;
    margin-top: .5rem;
    text-align: left;
}
.post-content-title-input input{
    height: 1.5rem;
    width: 15rem;
    text-align: left;
}
.post-content-body{
    width: 80%;
    display: flex;
    margin-left: -1rem;
    text-align: left; 
}
.post-content-body-body{
    width: 10%;
    height: 2rem;
}
.post-content-body-textarea{
    width: 90%;
    margin-bottom:2rem;
    margin-top:1rem;
    text-align: left;
}
.post-content-body-textarea textarea{
    width: 100%;
    height: 10rem;
    text-align: left;
}
.post-image{
    width: 100%;
    height: 2rem;
    text-align: left;
    margin-left: 9rem;

}
.post-button{
    width: 80%;
    height: 2rem;
    text-align: end;
}
</style>