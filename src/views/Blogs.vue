<template>
  <div class="blog-container">
    <div class="blogs-posted" v-for="post in blogsPosted" :key="post.id">
        <div class="blogs_img" :style="post.image"></div>
         <div class="blogs_title">
           <h3>{{post.title}}</h3>
         </div>
       </div>
      </div>
</template>
<script>

export default {
  name: 'Blogs',
  data(){
    return{
     blogsPosted: [
          {
          id: '1',
          title: 'Robots & Unemployability',
          image: {
            background: 'url('+require('../assets/robot3.jpg')+')',
            backgroundSize: 'cover',
            backgroundPosition: 'center',
            backgroundRepeat: 'no-repeat',
            width: '100%',
            height: '80%',
          },
        },
        {
          id: '2',
          title: 'Human’s human',
          image: {
            background: 'url('+require('../assets/robot4.jpg')+')',
            backgroundSize: 'cover',
            backgroundPosition: 'center',
            backgroundRepeat: 'no-repeat',
            width: '100%',
            height: '80%',
          },
        },
        {
          id: '3',
          title: 'Robots can be friendly',
          image: {
            background: 'url('+require('../assets/robot5.jpg')+')',
            backgroundSize: 'cover',
            backgroundPosition: 'center',
            backgroundRepeat: 'no-repeat',
            width: '100%',
            height: '80%',
          },
        },
        {
          id: '4',
          title: 'Human’s human',
          image: {
            background: 'url('+require('../assets/robot4.jpg')+')',
            backgroundSize: 'cover',
            backgroundPosition: 'center',
            backgroundRepeat: 'no-repeat',
            width: '100%',
            height: '80%',
          },
        },
        {
          id: '5',
          title: 'Robots can be friendly',
          image: {
            background: 'url('+require('../assets/robot5.jpg')+')',
            backgroundSize: 'cover',
            backgroundPosition: 'center',
            backgroundRepeat: 'no-repeat',
            width: '100%',
            height: '80%',
          },
        },
        {
          id: '6',
          title: 'Robots & Unemployability',
          image: {
            background: 'url('+require('../assets/robot3.jpg')+')',
            backgroundSize: 'cover',
            backgroundPosition: 'center',
            backgroundRepeat: 'no-repeat',
            width: '100%',
            height: '80%',
          },
        },
        ]
    }
  }
}
</script>
<style>
.blog-container{
  width: 100%;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  align-items: left;
  background-color: #C4C4C4;
  opacity: .9;
  margin-top: 4rem;
}
.blogs-posted {
  display: inline-block;
  width: 20rem;
  height: 15rem;
  margin-left: 3rem;
  margin-top: 1rem;
  margin-bottom: 3rem;
  background: linear-gradient(180deg, rgba(46, 45, 45, 0) 0%, #202020 100%);
  color: rgb(255, 255, 255);
}
.blogs_title{
  text-align: left;
  margin-left: .5rem;
  margin-top: -.5rem;
}
.blogs_img{
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  width: 100%;
  height: 80%;
  cursor: pointer;
}
</style>