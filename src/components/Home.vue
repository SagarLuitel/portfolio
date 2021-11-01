<template>
    <div class="container">
        <div class="navbar">
            <div class="logo">Sagar Luitel</div>
            <div class="right">
                <ul>
                    <li><a href="#section1">Home</a></li>
                    <li><a href="#section2">Techsatck</a></li>
                    <li><a href="#section3">About</a></li>
                    <li> <a href="#section4">Projects</a> </li>
                    <li> <a href="#section5">Contact</a></li>
                </ul>
            </div>
        </div>
        <div class="home" id="section1">
            <div class="info" >
                <img alt="Sagar" src=".././assets/logo.png">
                <div>
                    <h2>Sagar Luitel</h2>
                    <h3>Junior Software Engineer</h3>  
                </div>   
            </div>
            <div class="icons">
               <a href="https://www.linkedin.com/in/sagarluitel/">  <fa :icon="['fab','linkedin']" class="icon"/> </a>
               <a href="https://github.com/SagarLuitel/"><fa :icon="['fab','github']" class="icon"/></a>
            </div>
        </div>

        <div class="techstack" id="section2">
            <h2>Techstack</h2>
            <img alt="" src=".././assets/htmllogo.png" class="stackIcon">
            <img alt="" src=".././assets/csslogo.jpeg" class="stackIcon">
            <img alt="" src=".././assets/bootstraplogo.png" class="stackIcon">
            <img alt="" src=".././assets/jslogo.jpeg" class="stackIcon">
            <img alt="" src=".././assets/reactjslogo.png" class="stackIcon">
            <img alt="" src=".././assets/vuejslogo.jpeg" class="stackIcon">
            <img alt="" src=".././assets/javalogo.png" class="stackIcon">
            <img alt="" src=".././assets/nodelogo.png" class="stackIcon">
            <img alt="" src=".././assets/postgreslogo.png" class="stackIcon">
            <img alt="" src=".././assets/mongologo.png" class="stackIcon">


        </div>

        <div class="about" id="section3">
            <div class="introduction detail">
                <h3>Introduction</h3>
                <h4>Introduction</h4>
            </div>
            <div class="education detail">
                <h3>Education Background</h3>
                <h4>Introduction</h4>
            </div>
            <div class="experience detail">
                <h3>Professional Experience</h3>
                <h4>Introduction</h4>
            </div>
            
        </div>
        <h4>For more info on me,download my
                <a href=".././assets/Resume-SagarLuitel.pdf" target="_blank" id="action-link">resume</a>
        </h4>
        <div class="projects" id="section4">
            <h2>Completed Projects</h2>
            <div class="projectWrapper">
                <div class=" detail">
                    <h3>Introduction</h3>
                    <h4>Introduction</h4>
                </div>
                <div class=" detail">
                    <h3>Education Background</h3>
                    <h4>Introduction</h4>
                </div>
                <div class=" detail">
                    <h3>Professional Experience</h3>
                    <h4>Introduction</h4>
                </div>
            </div>
            
        </div>
        <div class="contact" id="section5">
            <h3>Get in touch with me to discuss any potential opportunity or colloboration.</h3>
            <form action="https://formsubmit.co/luitelsg@gmail.com" method="POST">
                <input type="text" name="name" required placeholder="Name">
                <input type="email" name="email" placeholder="Email Address"  required>
                <input type="textarea" name="text" required wrap="hard" placeholder="Enter your message here...." class="textarea">
                <input type="hidden" name="_subject" value="New submission!">
                <input type="hidden" name="_autoresponse" value="Hi There! 
                Thank you for your email. 
                I'll get back to you as soon as possible. 
                Regards,
                Sagar Luitel">
                <button type="submit">Send</button>
            </form>
        </div>
  </div>

</template>

<script>
export default {
  name: 'Home',
}
</script>

<style scoped>
/* Navbar Styling */
.navbar{
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin:0 30px;
    position: sticky;
    top: 0;
    background: white;
    z-index: 12;
}

ul {
  list-style-type: none;
  display: flex;
  justify-content: space-evenly;
  align-content: center;
}
li {
  width: 70px;
  margin: 0 20px;
  padding: 10px 6px;
  cursor: pointer;
  align-items: center;
}
a{
    text-decoration: none;
    color: black;
}

li:hover{
    background-color: #42b983;
    border-radius: 10px;
}

nav ul li a.current {
  background: black;
}
/* Home Styling */

.home{
    padding-top: 70px;
}

.info{
    display: flex;
    justify-content: center;
    align-items: center;
}

.icon{
    height: 2rem;
    width: 2rem;
    margin: 0 1rem;
    color:#42b983;
}
/* Techsatck styling */
.techstack{
    margin: 1rem;
    background: white;
    padding-top: 50px;
}

.stackIcon{
    height: 65px;
    width: 65px;
    background-color: white;
    margin: 8px;
}
/* about styling */
.about{
    display: flex;
    justify-content: center;
    align-items: center;
    padding-top: 70px;

}

.detail{
    border: 0.5px dotted #42b983;
    height:300px;
    width:400px;
    margin: 16px 10px;
}

.detail:hover{
    height:310px;
    width:410px;
}
/* project styling */
.projects{
    padding-top:30px;

}

.details{
background-image: url(".././assets/mongologo.png");
}

.projectWrapper{
    display: flex;
    justify-content: center;
    align-items: center;
}
/* contact styling */
form{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

input{
    margin: 10px;
    height:20px;
    width:400px;
    border-color: #42b983;
}

form>button{
    height:35px;
    width:90px;
    border-radius: 10px;
}

button:hover{
    background-color: #42b983;
}

.textarea{
height:130px;
padding: 0;
}
</style>
