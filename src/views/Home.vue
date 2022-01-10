<template>
  <div class="home">
    <div class="top" :style="bg">
      <div class="left_tag">
        <p class="p1">The future depends on Robots.</p>
        <p class="p2">Robots are the future</p> 
        <p class="p3">Human Beings.</p>
      </div>
      <div class="right_tag">
        <p class="p1">I am here to help.</p>
      </div>
    </div>
    <div class="center">
      <h3>What do you think of the future?</h3>
        <div class="center_left">
        <p>Robots are tools that can autonomously sense, reason, plan, and action. As well as performing tasks independently, they can also extend human capabilities, and mimic human actions. Ultimately, the word robot is derived from the Czech word robota, meaning forced labour.</p>
      </div>
      <div class="center_right" :style="sideImage">
        </div>  
    </div>
    <div class="bottom">
      <div class="bottom_h3">
        <h3>Blogs</h3>
      </div>
      <div class="blogs" v-for="blog in blogs" :key="blog.id">
        <div class="blog_img" :style="blog.image"></div>
         <div class="blog_title">
           <h3>{{blog.title}}</h3>
         </div>
       </div>
       <div class="more_blogs">
         <button @click="blogsClicked">More</button>
       </div>
    </div>    
  </div>
</template>

<script>

export default {
  name: 'Home',
  data(){
     return {
       bg: {
          background: 'url('+require('../assets/robot.jpg')+')',
          backgroundSize: 'cover',
          backgroundPosition: 'center',
          backgroundRepeat: 'no-repeat',
          height: '80vh',
          width: '100%',
          position: 'relative',
          top: '-2rem',
          margin: '0',
          zIndex: '-1'
        },
        sideImage: {
          background: 'url('+require('../assets/robot2.jpg')+')',
          backgroundSize: 'cover',
          backgroundPosition: 'center',
          backgroundRepeat: 'no-repeat',
          height: '75vh',
          width: '65vh',
          top: '87%',
          marginTop: '4rem',
          marginLeft: '50%'
        },
        blogs: [
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
   },
   methods: {
     blogsClicked(){
       this.$router.push('/blogs')
     }
   }
}
</script>
<style scoped>
.left_tag p.p1{
  font-size: 1.1rem;
  color: #fff;
  position: absolute;
  top: 30%;
  left: 16%;
  font-weight: bold;
  z-index: 1; 
}
.left_tag p.p2{
  font-size: 1.1rem;
  color: #fff;
  position: absolute;
  top: 34%;
  left: 21.5%;
  font-weight: bold;
  z-index: 1; 
}
.left_tag p.p3{
  font-size: 1.1rem;
  color: #fff;
  position: absolute;
  top: 38%;
  left: 25.5%;
  font-weight: bold;
  z-index: 1; 
}
.right_tag p.p1{
  font-size: 1.1rem;
  color: #fff;
  position: absolute;
  top: 49%;
  left: 72%;
  font-weight: bold;
  z-index: 1; 
}
.center{
  background-color: #C4C4C4;
  color: #000;
  height: 100vh;
  width: 100%;
  margin-top: -6rem;
}
.center h3{
  font-size: 1rem;
  font-weight: bold;
  text-align: center;
  padding-top: 2rem;
}
.center_left{
  float: left;
  text-align: left;
  width: 34%;
  height: 40%;
  margin-left: 6%;
  margin-top: 10rem;
  font: 1.5rem 'Roboto', sans-serif;

}
.bottom{
  width: 100%;
  background-color: #c4c4c4;
}
.bottom_h3{
    text-align: center;
    margin-top: -2.5rem;
    font: 2em sans-serif;
    font-weight: bolder;
}
.blogs{
  display: inline-block;
  width: 22rem;
  height: 20rem;
  margin-left: 3rem;
  margin-right: 3rem;
  margin-top: 2rem;
  background-color: #666666;
  margin-bottom: 10%;
  background: linear-gradient(180deg, rgba(46, 45, 45, 0) 0%, #202020 100%);
  color: rgb(255, 255,255);
}
.blog_img{
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  width: 100%;
  height: 80%;
  cursor: pointer;
}
.blog_title{
  text-align: left;
  margin-left: .5rem;
}
.more_blogs{
  text-align: center;
  margin-top: -5rem;
}
.more_blogs button{
  background-color: #666666;
  text-align: center;
  width: 7rem;
  font-size: 1.1rem;
  color: #fff;
  border-radius: 5px;
  margin-bottom: 10%;
  cursor: pointer;

}
</style>