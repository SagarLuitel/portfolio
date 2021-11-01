<template>
    <div class="container">
        <header :class="{'scrolled-nav': scrollNav}">
            <nav>
                <div class="logo"><img src=".././assets/sagarlogo.png" alt=""></div>
                <ul v-show="!mobile" class="navigation">
                    <li>
                        <a href="#home" :class="{ barActive: tabOption === 'home' }"
                        @click="tabOption = 'home'">Home</a>
                    </li>
                    <li>
                        <a href="#techstack" :class="{ barActive: tabOption === 'techstack' }"
                        @click="tabOption = 'techstack'">Techstack</a>
                    </li>
                    <li>
                        <a href="#about" :class="{ barActive: tabOption === 'about' }"
                        @click="tabOption = 'about'">About</a>
                    </li>
                    <li> 
                        <a href="#projects" :class="{ barActive: tabOption === 'projects' }"
                        @click="tabOption = 'projects'">Projects</a> 
                    </li>
                    <li> 
                        <a href="#contact" :class="{ barActive: tabOption === 'contact' }"
                        @click="tabOption = 'contact'">Contact</a>
                    </li>
                </ul>
                <div  class="toggleicon">
                    <i @click="toggleMobileNav" v-show="mobile" class="fas fa-bars" :class="{'icon-active' : mobileNav}"> </i>
                </div>
                <transition name="mobile-nav">
                    <ul v-show="mobileNav" class="dropdown-nav">
                    <li>
                        <a href="#home" :class="{ barActive: tabOption === 'home' }"
                        @click="tabOption = 'home'" >Home</a>
                    </li>
                    <li>
                        <a href="#techstack"  :class="{ barActive: tabOption === 'techstack'}" 
                        @click="tabOption = 'techstack'" >Techstack</a>
                    </li>
                    <li>
                        <a href="#about" :class="{ barActive: tabOption === 'about' }"
                        @click="tabOption = 'about'">About</a>
                    </li>
                    <li> 
                        <a href="#projects" :class="{ barActive: tabOption === 'projects' }"
                        @click="tabOption = 'projects'">Projects</a> 
                    </li>
                    <li> 
                        <a href="#contact" :class="{ barActive: tabOption === 'contact' }"
                        @click="tabOption = 'contact'">Contact</a>
                    </li>
                </ul>
                </transition>
                    
            
        </nav>
        </header>
        
        <div class="home" id="home">
            <div class="info" >
                <img alt="Sagar" src=".././assets/SagarPic.png" class="profilepic">
                <div>
                    <h1>Sagar Luitel</h1>
                    <h3>
                        <span class="typed-text">{{ typeValue }}</span>
                        <span class="cursor" :class="{'typing': typeStatus}">&nbsp;</span>
                        </h3>  
                </div>   
            </div>
            <div class="icons">
               <a href="https://www.linkedin.com/in/sagarluitel/">  <fa :icon="['fab','linkedin']" class="icon"/> </a>
               <a href="https://github.com/SagarLuitel/"><fa :icon="['fab','github']" class="icon"/></a>
            </div>
        </div>

        <div class="techstack" id="techstack">
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
        <div class="about" id="about">
         <h3>About Me </h3> 
        <div class="about-wrapper">
            <div class="introduction detail">
                <h3>Introduction</h3>
                <h4>I am a full stack developer. I strive  to write clean, structured and maintainable codes.  I also am a quick learner and I love exploring new technology. I enjoy working in a team as well as self directed setting. Being an Information Systems graduate, I have a good formal understanding of OOP concepts and programming principles. I value continuous learning and upgrading myself, teaching others and learning from others.
</h4>
            </div>
            <div class="education detail">
                <h3>Education Background</h3>
                <h4>I am a recent Information Systems graduate with a minor in software development. During my study, I got the opportunity to learn software development, data structure and algorithm, distributed systems and enterprise computing. These courses made me realise my interest in software engineering. I also have a formal education in business administration and marketing.
</h4>
            </div>
            <div class="experience detail">
                <h3>Professional Experience</h3>
                <h4>For the past two years, I have been working as a support and analyst contractor while continuing my studies. This has given me wonderful opportunities to travel to different sites, meet new people and work on diverse projects ranging from setting up IT infrastructures to providing IT  support to different clients. Similarly, I also have experience working in financial industry as a business analyst.</h4>
            </div>
            
        </div>
        </div>
        
        <div class="projects" id="projects">
            <h2>Completed Projects</h2>
            <div class="projectWrapper">
                <div class="project1 projectBox">
                    <img alt="" src=".././assets/snakegame.png" class="detail">
                    <div class="projectDesc">My take on classic snake game. Wouldn't it be exciting if only instead of eating food, the snake had to compete for food and hide from its predator. <div>Completing using: HTML, CSS, Javascript</div></div>
                </div>
                <div class="project2  projectBox">
                    <img alt="" src=".././assets/moviechat.png" class="detail"> 
                    <div class="projectDesc">Site where users can chat about their favourite movie. Import movie from IMdb and give comments and feedback on realtime on each movie. <div>Completed using: React, Express, PostgreSql, Bootstrap, Netlify, Heroku, SocketIO</div></div>
                </div>
                <div class="project3  projectBox">
                    <img alt="" src=".././assets/babybarn.png" class="detail">
                    <div class="projectDesc">E-commerce site for kids. Find all category of items needed for keeds in this one stop website.   <div>Completed React, Redux, Express, MongoDB, MaterialUI, Netfily, Heroku</div></div>
                </div>
                <div class="project4 projectBox ">
                    <img alt="" src=".././assets/Blog.png" class="detail">
                    <div class="projectDesc">This project is something that i made for my personal use. This is a blog which i intend to use to post new contents in my software engineering journey.  <div>Completed using: React, MongoDB, Express, MaterialUi</div> </div>
                </div>
            </div>
            
        </div>
        <div class="contact" id="contact">
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
        <footer>© 2021 Sagar Luitel</footer>
  </div>

</template>

<script>
export default {
  name: 'Duplicate',

  data(){
      return{
          scrolledNav: null,
          mobile: null,
          mobileNav: null,
          windowWidth: null,
          typeValue: '',
          typeStatus: false,
          typeArray: ['Junior Software Engineer', 'Recent Graduate', 'Full Stack Developer'],
          typingSpeed: 200,
          erasingSpeed: 100,
          newTextDelay: 2000,
          typeArrayIndex: 0,
          charIndex: 0,
          tabOption: "home"
      };
  },
  created() {
      window.addEventListener('resize', this.checkScreen);
      this.checkScreen();
      setTimeout(this.typeText, this.newTextDelay + 200);
  },
  mounted(){
      window.addEventListener("scroll", this.updateScroll)
  },
  methods: {
      toggleMobileNav(){
          this.mobileNav=!this.mobileNav;
      },

     updateScroll(){
         const scrollPosition = window.scrollY;
         if(scrollPosition>50){
             this.scrolledNav = true;
             return true;
         }
         this.scrolledNav = false;
     },
      checkScreen(){
          this.windowWidth = window.innerWidth;
          if(this.windowWidth <= 750){
              this.mobile = true;
              return;
          }
          this.mobile = false;
          this.mobileNav = false;
          return;
      },
      typeText() {
        if(this.charIndex < this.typeArray[this.typeArrayIndex].length) {
          if(!this.typeStatus)
            this.typeStatus = true;
          this.typeValue += this.typeArray[this.typeArrayIndex].charAt(this.charIndex);
          this.charIndex += 1;
          setTimeout(this.typeText, this.typingSpeed);
        }
        else {
          this.typeStatus = false;
          setTimeout(this.eraseText, this.newTextDelay);
        }
      },
      eraseText() {
        if(this.charIndex > 0) {
          if(!this.typeStatus)
            this.typeStatus = true;
          this.typeValue = this.typeArray[this.typeArrayIndex].substring(0, this.charIndex - 1);
          this.charIndex -= 1;
          setTimeout(this.eraseText, this.erasingSpeed);
        }
        else {
          this.typeStatus = false;
          this.typeArrayIndex += 1;
          if(this.typeArrayIndex >= this.typeArray.length)
            this.typeArrayIndex = 0;
          setTimeout(this.typeText, this.typingSpeed + 1000);
        }
      }
    },
}
</script>

<style scoped>
/* Navbar Styling */
header{
    color: #42b983;
    z-index: 99;
    width: 100%;
    position: fixed;
    transition: .5s ease all;
    background-color: white;
}

nav{
    display:flex;
    flex-direction: row;
    transition: .5s ease all;
    width: 90%;
    margin: 0 auto;
    position: relative;
    padding: 0;
   
}

.navigation{
    display:flex;
    align-items: center;
    flex: 1;
    justify-content: flex-end;
}

.logo{
    display: flex;
    align-items: center;
}

.logo>img{
    width:50px;
    transition: .5s ease all;
}

.profilepic{
    height: 276px;
    width: 185px;
    padding-bottom: 1rem;
}

li{
    text-transform: uppercase;
    padding: 16px;
    margin-left: 16px;
}

a{
    font-size: 16px;
    font-weight: 500;
    transform: 0.5s ease all;
    padding-bottom: 4px;
    border-bottom: 1px solid transparent;
}

a:hover{
    border-color: #42b983;
}

.toggleicon{
    display: flex;
    align-items: center;
    position: absolute;
    top:0;
    right: 24px;
    height:100%
}

.toggleicon>i{
    cursor: pointer;
    font-size: 24px;
    transition: 0.8s ease all;
}

.icon-active{
    transform: rotate(180deg);
}

ul,li,a{
    text-decoration: none;
    list-style: none;
    color: #42b983;

}



.dropdown-nav{
    display: flex;
    flex-direction: column;
    position: fixed;
    width:100%;
    max-width: 250px;
    height:100%;
    background-color: white ;
    top:0;
    left:0;
    margin: 0;
}

.dropdown-nav>li{
    margin-left:0;
    
}

a.barActive{
  transition: all 0.3s linear;
  border-bottom: 1px solid #42b983;
}

.dropdown-nav a{
    color: black;
}

.scrolled-nav{
    background-color: black;
}

.mobile-nav-enter-active,
.mobile-nav-leave-active{
    transition: 1s ease all;
}

.mobile-nav-enter-from,
.mobile-nav-leave-to{
    transform: translateX(-250px);
}

.mobile-nav-enter-to{
    transform: translateX(0);
}

span.typed-text {
      color: #42b983;
    }

@media(min-width: 1140px){
    .nav{
        max-width: 1140px;
    }
}
/* Home Styling */

.home{
    padding-top: 80px;
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
    background: white;
    padding-top: 75px;
}

.stackIcon{
    height: 65px;
    width: 65px;
    background-color: white;
    margin: 8px;
}

@media (max-width: 750px) {
  .stackIcon {
    height: 55px;
    width: 55px;
  }
}

/* about styling */
.about{
    
    padding-top: 70px;

}

.about-wrapper{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
}

h4{
    text-align: justify;
    padding: 0 5px;
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
    padding-top:60px;

}

.projectDesc{
    text-align: justify;
    padding: 5px;
}

.projectWrapper{
    display: flex;
    justify-content: center;
    align-items: center;
     flex-wrap: wrap;
}


.projectBox{
    border: 0.5px dotted #42b983;
    height:500px;
    width:420px;
    margin: 16px 10px;
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

/* footer styleing */

footer{
    border-top: 2px solid #42b983;
    margin: 40px;
    font-weight: 600;
}
</style>
