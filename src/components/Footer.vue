<template>
    <div class="footer">
        <div class="footer-content">
            <div class="site_logo">
                <h1>RoBlog</h1>
                <p class="logo_name">
                    <span>RoBlog</span><br>
                    <span>2021</span>
                </p>
            </div>
            <div class="links">
                <div class="link_left">
                    <h3>Blogs</h3>
                    <p>Robotics</p>
                    <p>Metaverse</p>
                    <p>Autonomous</p>
                    <p>Humanoid Robot</p>
                </div>
                <div class="link_center">
                    <h3>Articles</h3>
                    <p>Anthropomorphism</p>
                    <p>Healthcare Robotics</p>
                    <p>Google's Worker Robots</p>
                    <p>Artificial Intelligence</p>
                </div>
                <div class="link_right">
                    <h3>Legal Terms</h3>
                    <p>Privacy Policy</p>
                    <p>Terms of Use</p>
                </div>
            </div>
        </div>
        <div class="footer-bottom">
            &copy; RoBlog.com | Designed by RoBlog
        </div>
    </div>
</template>

<script>
export default {
    name: 'Footer'

}
</script>

<style>
.footer {
    background-color: #666666;
    color: #fff;
    height: 30vh;
    text-align: center;
}
.footer-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
}
.site_logo {
    float: left;
    font: 1em sans-serif;
    margin-left: 5rem;
    margin-top: -5rem;
    margin-bottom: 0;
}
.logo_name {
    margin-top: -1rem;
}
.links {
    display: flex;
    align-self: start;
    justify-content: space-between;
    text-align: left;
}
.link_left {
    margin: 0px;
    margin-right: 250px;
    text-align: left;
}
.link_left p{
    font-size: .8em;
    text-align: left;
}
.link_center {
    margin: 0px;
    margin-right: 250px;
    text-align: left;
}
.link_center p{
    font-size: .8em;
    text-align: left;
}
.link_right {
    margin: 0px;
    margin-right: 200px;
}
.link_right p{
    font-size: .8em;
}
.footer-bottom {
    font-size: 0.8em;
    margin-top: 10px;
}

</style>