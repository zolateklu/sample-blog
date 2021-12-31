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
         <button>More</button>
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
          top: '-4.5rem',
          margin: '0',
          zIndex: '-1'
        },
        sideImage: {
          background: 'url('+require('../assets/robot2.jpg')+')',
          backgroundSize: 'cover',
          backgroundPosition: 'center',
          backgroundRepeat: 'no-repeat',
          height: '75vh',
          width: '70vh',
          position: 'absolute',
          top: '87%',
          left: '50%',
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
   }
}
</script>
<style scoped>
.left_tag p.p1{
  font-size: 1.1rem;
  color: #fff;
  position: absolute;
  top: 34%;
  left: 8%;
  font-weight: bold;
  z-index: 1; 
}
.left_tag p.p2{
  font-size: 1.1rem;
  color: #fff;
  position: absolute;
  top: 38%;
  left: 16%;
  font-weight: bold;
  z-index: 1; 
}
.left_tag p.p3{
  font-size: 1.1rem;
  color: #fff;
  position: absolute;
  top: 42%;
  left: 22%;
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
  height: 80%;
  margin-left: 6%;
  margin-top: 4%;
  font: 1.5rem 'Roboto', sans-serif;

}
.blogs{
  display: inline-block;
  width: 30%;
  height: 40vh;
  margin-left: 2%;
  margin-top: 2%;
  background-color: #666666;
  margin-bottom: 10%;
  color: rgb(44, 44, 44)
}
.blog_title{
  text-align: left;
}
.more_blogs button{
  background-color: #666666;
  text-align: center;
  width: 7rem;
  font-size: 1.1rem;
  color: #fff;
  border-radius: 5px;
  margin-bottom: 10%;

}
</style>