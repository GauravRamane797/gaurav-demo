# gaurav-demo
<!DOCTYPE html>
<!-- Created By CodingNepal -->
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Personal Portfolio Website</title>
    <link rel="stylesheet" href="style.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css"/>
    <script src="https://code.jquery.com/jquery-3.5.1.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/typed.js/2.0.11/typed.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/waypoints/4.0.1/jquery.waypoints.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/OwlCarousel2/2.3.4/owl.carousel.min.js"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/OwlCarousel2/2.3.4/assets/owl.carousel.min.css"/>

</head>
<style>
  /*  import google fonts */
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&family=Ubuntu:wght@400;500;700&display=swap');

*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    text-decoration: none;
}
html{
    scroll-behavior: smooth;
}

/* custom scroll bar */
::-webkit-scrollbar {
    width: 10px;
}
::-webkit-scrollbar-track {
    background: #f1f1f1;
}
::-webkit-scrollbar-thumb {
    background: #888;
}

::-webkit-scrollbar-thumb:hover {
    background: #555;
}

/* all similar content styling codes */
section{
    padding: 100px 0;
}
.max-width{
    max-width: 1300px;
    padding: 0 80px;
    margin: auto;
}
.about, .services, .skills, .teams, .contact, footer{
    font-family: 'Poppins', sans-serif;
}
.about .about-content,
.services .serv-content,
.skills .skills-content,
.contact .contact-content{
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: space-between;
}
section .title{
    position: relative;
    text-align: center;
    font-size: 40px;
    font-weight: 500;
    margin-bottom: 60px;
    padding-bottom: 20px;
    font-family: 'Ubuntu', sans-serif;
}
section .title::before{
    content: "";
    position: absolute;
    bottom: 0px;
    left: 50%;
    width: 180px;
    height: 3px;
    background: #111;
    transform: translateX(-50%);
}
section .title::after{
    position: absolute;
    bottom: -8px;
    left: 50%;
    font-size: 20px;
    color: crimson;
    padding: 0 5px;
    background: #fff;
    transform: translateX(-50%);
}

/* navbar styling */
.navbar{
    position: fixed;
    width: 100%;
    z-index: 999;
    padding: 30px 0;
    font-family: 'Ubuntu', sans-serif;
    transition: all 0.3s ease;
}
.navbar.sticky{
    padding: 15px 0;
    background: crimson;
}
.navbar .max-width{
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.navbar .logo a{
    color: #fff;
    font-size: 35px;
    font-weight: 600;
}
.navbar .logo a span{
    color: crimson;
    transition: all 0.3s ease;
}
.navbar.sticky .logo a span{
    color: #fff;
}
.navbar .menu li{
    list-style: none;
    display: inline-block;
}
.navbar .menu li a{
    display: block;
    color: #fff;
    font-size: 18px;
    font-weight: 500;
    margin-left: 25px;
    transition: color 0.3s ease;
}
.navbar .menu li a:hover{
    color: crimson;
}
.navbar.sticky .menu li a:hover{
    color: #fff;
}

/* menu btn styling */
.menu-btn{
    color: #fff;
    font-size: 23px;
    cursor: pointer;
    display: none;
}
.scroll-up-btn{
    position: fixed;
    height: 45px;
    width: 42px;
    background: crimson;
    right: 30px;
    bottom: 10px;
    text-align: center;
    line-height: 45px;
    color: #fff;
    z-index: 9999;
    font-size: 30px;
    border-radius: 6px;
    border-bottom-width: 2px;
    cursor: pointer;
    opacity: 0;
    pointer-events: none;
    transition: all 0.3s ease;
}
.scroll-up-btn.show{
    bottom: 30px;
    opacity: 1;
    pointer-events: auto;
}
.scroll-up-btn:hover{
    filter: brightness(90%);
}


/* home section styling */
.home{
    display: flex;
    background: url("images/banner.jpg") no-repeat center;
    height: 100vh;
    color: #fff;
    min-height: 500px;
    background-size: cover;
    background-attachment: fixed;
    font-family: 'Ubuntu', sans-serif;
}
.home .max-width{
  width: 100%;
  display: flex;
}
.home .max-width .row{
  margin-right: 0;
}
.home .home-content .text-1{
    font-size: 27px;
}
.home .home-content .text-2{
    font-size: 75px;
    font-weight: 600;
    margin-left: -3px;
}
.home .home-content .text-3{
    font-size: 40px;
    margin: 5px 0;
}
.home .home-content .text-3 span{
    color: crimson;
    font-weight: 500;
}
.home .home-content a{
    display: inline-block;
    background: crimson;
    color: #fff;
    font-size: 25px;
    padding: 12px 36px;
    margin-top: 20px;
    font-weight: 400;
    border-radius: 6px;
    border: 2px solid crimson;
    transition: all 0.3s ease;
}
.home .home-content a:hover{
    color: crimson;
    background: none;
}

/* about section styling */
.about .title::after{
    content: "who i am";
}
.about .about-content .left{
    width: 45%;
}
.about .about-content .left img{
    height: 400px;
    width: 400px;
    object-fit: cover;
    border-radius: 6px;
}
.about .about-content .right{
    width: 55%;
}
.about .about-content .right .text{
    font-size: 25px;
    font-weight: 600;
    margin-bottom: 10px;
}
.about .about-content .right .text span{
    color: crimson;
}
.about .about-content .right p{
    text-align: justify;
}
.about .about-content .right a{
    display: inline-block;
    background: crimson;
    color: #fff;
    font-size: 20px;
    font-weight: 500;
    padding: 10px 30px;
    margin-top: 20px;
    border-radius: 6px;
    border: 2px solid crimson;
    transition: all 0.3s ease;
}
.about .about-content .right a:hover{
    color: crimson;
    background: none;
}

/* services section styling */
.services, .teams{
    color:#fff;
    background: #111;
}
.services .title::before,
.teams .title::before{
    background: #fff;
}
.services .title::after,
.teams .title::after{
    background: #111;
    content: "what i provide";
}
.services .serv-content .card{
    width: calc(33% - 20px);
    background: #222;
    text-align: center;
    border-radius: 6px;
    padding: 50px 25px;
    cursor: pointer;
    transition: all 0.3s ease;
}
.services .serv-content .card:hover{
    background: crimson;
}
.services .serv-content .card .box{
    transition: all 0.3s ease;
}
.services .serv-content .card:hover .box{
    transform: scale(1.05);
}
.services .serv-content .card i{
    font-size: 50px;
    color: crimson;
    transition: color 0.3s ease;
}
.services .serv-content .card:hover i{
    color: #fff;
}
.services .serv-content .card .text{
    font-size: 25px;
    font-weight: 500;
    margin: 10px 0 7px 0;
}

/* skills section styling */

.skills .title::after{
    content: "what i know";
}
.skills .skills-content .column{
    width: calc(50% - 30px);
}
.skills .skills-content .left .text{
    font-size: 20px;
    font-weight: 600;
    margin-bottom: 10px;
}
.skills .skills-content .left p{
    text-align: justify;
}
.skills .skills-content .left a{
    display: inline-block;
    background: crimson;
    color: #fff;
    font-size: 18px;
    font-weight: 500;
    padding: 8px 16px;
    margin-top: 20px;
    border-radius: 6px;
    border: 2px solid crimson;
    transition: all 0.3s ease;
}
.skills .skills-content .left a:hover{
    color: crimson;
    background: none;
}
.skills .skills-content .right .bars{
    margin-bottom: 15px;
}
.skills .skills-content .right .info{
    display: flex;
    margin-bottom: 5px;
    align-items: center;
    justify-content: space-between;
}
.skills .skills-content .right span{
    font-weight: 500;
    font-size: 18px;
}
.skills .skills-content .right .line{
    height: 5px;
    width: 100%;
    background: lightgrey;
    position: relative;
}
.skills .skills-content .right .line::before{
    content: "";
    position: absolute;
    height: 100%;
    left: 0;
    top: 0;
    background: crimson;
}
.skills-content .right .html::before{
    width: 90%;
}
.skills-content .right .css::before{
    width: 60%;
}
.skills-content .right .js::before{
    width: 80%;
}
.skills-content .right .php::before{
    width: 50%;
}
.skills-content .right .mysql::before{
    width: 70%;
}

/* teams section styling */
.teams .title::after{
    content: "who with me";
}
.teams .carousel .card{
    background: #222;
    border-radius: 6px;
    padding: 25px 35px;
    text-align: center;
    overflow: hidden;
    transition: all 0.3s ease;
}
.teams .carousel .card:hover{
    background: crimson;
}
.teams .carousel .card .box{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    transition: all 0.3s ease;
}
.teams .carousel .card:hover .box{
    transform: scale(1.05);
}
.teams .carousel .card .text{
    font-size: 25px;
    font-weight: 500;
    margin: 10px 0 7px 0;
}
.teams .carousel .card img{
    height: 150px;
    width: 150px;
    object-fit: cover;
    border-radius: 50%;
    border: 5px solid crimson;
    transition: all 0.3s ease;
}
.teams .carousel .card:hover img{
    border-color: #fff;
}
.owl-dots{
    text-align: center;
    margin-top: 20px;
}
.owl-dot{
    height: 13px;
    width: 13px;
    margin: 0 5px;
    outline: none!important;
    border-radius: 50%;
    border: 2px solid crimson!important;
    transition: all 0.3s ease;
}
.owl-dot.active{
    width: 35px;
    border-radius: 14px;
}
.owl-dot.active,
.owl-dot:hover{
    background: crimson!important;
}

/* contact section styling */
.contact .title::after{
    content: "get in touch";
}
.contact .contact-content .column{
    width: calc(50% - 30px);
}
.contact .contact-content .text{
    font-size: 20px;
    font-weight: 600;
    margin-bottom: 10px;
}
.contact .contact-content .left p{
    text-align: justify;
}
.contact .contact-content .left .icons{
    margin: 10px 0;
}
.contact .contact-content .row{
    display: flex;
    height: 65px;
    align-items: center;
}
.contact .contact-content .row .info{
    margin-left: 30px;
}
.contact .contact-content .row i{
    font-size: 25px;
    color: crimson;
}
.contact .contact-content .info .head{
    font-weight: 500;
}
.contact .contact-content .info .sub-title{
    color: #333;
}
.contact .right form .fields{
    display: flex;
}
.contact .right form .field,
.contact .right form .fields .field{
    height: 45px;
    width: 100%;
    margin-bottom: 15px;
}
.contact .right form .textarea{
    height: 80px;
    width: 100%;
}
.contact .right form .name{
    margin-right: 10px;
}
.contact .right form .field input,
.contact .right form .textarea textarea{
    height: 100%;
    width: 100%;
    border: 1px solid lightgrey;
    border-radius: 6px;
    outline: none;
    padding: 0 15px;
    font-size: 17px;
    font-family: 'Poppins', sans-serif;
    transition: all 0.3s ease;
}
.contact .right form .field input:focus,
.contact .right form .textarea textarea:focus{
    border-color: #b3b3b3;
}
.contact .right form .textarea textarea{
  padding-top: 10px;
  resize: none;
}
.contact .right form .button-area{
  display: flex;
  align-items: center;
}
.right form .button-area button{
  color: #fff;
  display: block;
  width: 160px!important;
  height: 45px;
  outline: none;
  font-size: 18px;
  font-weight: 500;
  border-radius: 6px;
  cursor: pointer;
  flex-wrap: nowrap;
  background: crimson;
  border: 2px solid crimson;
  transition: all 0.3s ease;
}
.right form .button-area button:hover{
  color: crimson;
  background: none;
}
/* footer section styling */
footer{
    background: #111;
    padding: 15px 23px;
    color: #fff;
    text-align: center;
}
footer span a{
    color: crimson;
    text-decoration: none;
}
footer span a:hover{
    text-decoration: underline;
}


/* responsive media query start */
@media (max-width: 1104px) {
    .about .about-content .left img{
        height: 350px;
        width: 350px;
    }
}

@media (max-width: 991px) {
    .max-width{
        padding: 0 50px;
    }
}
@media (max-width: 947px){
    .menu-btn{
        display: block;
        z-index: 999;
    }
    .menu-btn i.active:before{
        content: "\f00d";
    }
    .navbar .menu{
        position: fixed;
        height: 100vh;
        width: 100%;
        left: -100%;
        top: 0;
        background: #111;
        text-align: center;
        padding-top: 80px;
        transition: all 0.3s ease;
    }
    .navbar .menu.active{
        left: 0;
    }
    .navbar .menu li{
        display: block;
    }
    .navbar .menu li a{
        display: inline-block;
        margin: 20px 0;
        font-size: 25px;
    }
    .home .home-content .text-2{
        font-size: 70px;
    }
    .home .home-content .text-3{
        font-size: 35px;
    }
    .home .home-content a{
        font-size: 23px;
        padding: 10px 30px;
    }
    .max-width{
        max-width: 930px;
    }
    .about .about-content .column{
        width: 100%;
    }
    .about .about-content .left{
        display: flex;
        justify-content: center;
        margin: 0 auto 60px;
    }
    .about .about-content .right{
        flex: 100%;
    }
    .services .serv-content .card{
        width: calc(50% - 10px);
        margin-bottom: 20px;
    }
    .skills .skills-content .column,
    .contact .contact-content .column{
        width: 100%;
        margin-bottom: 35px;
    }
}

@media (max-width: 690px) {
    .max-width{
        padding: 0 23px;
    }
    .home .home-content .text-2{
        font-size: 60px;
    }
    .home .home-content .text-3{
        font-size: 32px;
    }
    .home .home-content a{
        font-size: 20px;
    }
    .services .serv-content .card{
        width: 100%;
    }
}

@media (max-width: 500px) {
    .home .home-content .text-2{
        font-size: 50px;
    }
    .home .home-content .text-3{
        font-size: 27px;
    }
    .about .about-content .right .text,
    .skills .skills-content .left .text{
        font-size: 19px;
    }
    .contact .right form .fields{
        flex-direction: column;
    }
    .contact .right form .name,
    .contact .right form .email{
        margin: 0;
    }
    .right form .error-box{
       width: 150px;
    }
    .scroll-up-btn{
        right: 15px;
        bottom: 15px;
        height: 38px;
        width: 35px;
        font-size: 23px;
        line-height: 38px;
    }
}

</style>
<body>
    <div class="scroll-up-btn">
        <i class="fas fa-angle-up"></i>
    </div>
    <nav class="navbar">
        <div class="max-width">
            <div class="logo"><a href="#">Portfo<span>lio.</span></a></div>
            <ul class="menu">
                <li><a href="#home" class="menu-btn">Home</a></li>
                <li><a href="#about" class="menu-btn">About</a></li>
                <li><a href="#services" class="menu-btn">Services</a></li>
                <li><a href="#skills" class="menu-btn">Skills</a></li>
                <li><a href="#teams" class="menu-btn">Teams</a></li>
                <li><a href="#contact" class="menu-btn">Contact</a></li>
            </ul>
            <div class="menu-btn">
                <i class="fas fa-bars"></i>
            </div>
        </div>
    </nav>

    <!-- home section start -->
    <section class="home" id="home">
        <div class="max-width">
            <div class="home-content">
                <div class="text-1">Hello, my name is</div>
                <div class="text-2">Prakash Shahi</div>
                <div class="text-3">And I'm a <span class="typing"></span></div>
                <a href="#">Hire me</a>
            </div>
        </div>
    </section>

    <!-- about section start -->
    <section class="about" id="about">
        <div class="max-width">
            <h2 class="title">About me</h2>
            <div class="about-content">
                <div class="column left">
                    <img src="images/profile-1.jpeg" alt="">
                </div>
                <div class="column right">
                    <div class="text">I'm Prakash and I'm a <span class="typing-2"></span></div>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quasi ut voluptatum eveniet doloremque autem excepturi eaque, sit laboriosam voluptatem nisi delectus. Facere explicabo hic minus accusamus alias fuga nihil dolorum quae. Explicabo illo unde, odio consequatur ipsam possimus veritatis, placeat, ab molestiae velit inventore exercitationem consequuntur blanditiis omnis beatae. Dolor iste excepturi ratione soluta quas culpa voluptatum repudiandae harum non.</p>
                    <a href="#">Download CV</a>
                </div>
            </div>
        </div>
    </section>

    <!-- services section start -->
    <section class="services" id="services">
        <div class="max-width">
            <h2 class="title">My services</h2>
            <div class="serv-content">
                <div class="card">
                    <div class="box">
                        <i class="fas fa-paint-brush"></i>
                        <div class="text">Web Design</div>
                        <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Rem quia sunt, quasi quo illo enim.</p>
                    </div>
                </div>
                <div class="card">
                    <div class="box">
                        <i class="fas fa-chart-line"></i>
                        <div class="text">Advertising</div>
                        <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Rem quia sunt, quasi quo illo enim.</p>
                    </div>
                </div>
                <div class="card">
                    <div class="box">
                        <i class="fas fa-code"></i>
                        <div class="text">Apps Design</div>
                        <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Rem quia sunt, quasi quo illo enim.</p>
                    </div>
                </div>
               </div>
            </div>
        </div>
    </section>

    <!-- skills section start -->
    <section class="skills" id="skills">
        <div class="max-width">
            <h2 class="title">My skills</h2>
            <div class="skills-content">
                <div class="column left">
                    <div class="text">My creative skills & experiences.</div>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Dignissimos, ratione error est recusandae consequatur, iusto illum deleniti quidem impedit, quos quaerat quis minima sequi. Cupiditate recusandae laudantium esse, harum animi aspernatur quisquam et delectus ipsum quam alias quaerat? Quasi hic quidem illum. Ad delectus natus aut hic explicabo minus quod.</p>
                    <a href="#">Read more</a>
                </div>
                <div class="column right">
                    <div class="bars">
                        <div class="info">
                            <span>HTML</span>
                            <span>90%</span>
                        </div>
                        <div class="line html"></div>
                    </div>
                    <div class="bars">
                        <div class="info">
                            <span>CSS</span>
                            <span>60%</span>
                        </div>
                        <div class="line css"></div>
                    </div>
                    <div class="bars">
                        <div class="info">
                            <span>JavaScript</span>
                            <span>80%</span>
                        </div>
                        <div class="line js"></div>
                    </div>
                    <div class="bars">
                        <div class="info">
                            <span>PHP</span>
                            <span>50%</span>
                        </div>
                        <div class="line php"></div>
                    </div>
                    <div class="bars">
                        <div class="info">
                            <span>MySQL</span>
                            <span>70%</span>
                        </div>
                        <div class="line mysql"></div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- teams section start -->
    <section class="teams" id="teams">
        <div class="max-width">
            <h2 class="title">My teams</h2>
            <div class="carousel owl-carousel">
                <div class="card">
                    <div class="box">
                        <img src="images/profile-1.jpeg" alt="">
                        <div class="text">Someone name</div>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
                    </div>
                </div>
                <div class="card">
                    <div class="box">
                        <img src="images/profile-2.jpeg" alt="">
                        <div class="text">Someone name</div>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
                    </div>
                </div>
                <div class="card">
                    <div class="box">
                        <img src="images/profile-3.jpeg" alt="">
                        <div class="text">Someone name</div>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
                    </div>
                </div>
                <div class="card">
                    <div class="box">
                        <img src="images/profile-4.jpeg" alt="">
                        <div class="text">Someone name</div>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
                    </div>
                </div>
                <div class="card">
                    <div class="box">
                        <img src="images/profile-5.jpeg" alt="">
                        <div class="text">Someone name</div>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- contact section start -->
    <section class="contact" id="contact">
        <div class="max-width">
            <h2 class="title">Contact me</h2>
            <div class="contact-content">
                <div class="column left">
                    <div class="text">Get in Touch</div>
                    <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Dignissimos harum corporis fuga corrupti. Doloribus quis soluta nesciunt veritatis vitae nobis?</p>
                    <div class="icons">
                        <div class="row">
                            <i class="fas fa-user"></i>
                            <div class="info">
                                <div class="head">Name</div>
                                <div class="sub-title">Prakash Shahi</div>
                            </div>
                        </div>
                        <div class="row">
                            <i class="fas fa-map-marker-alt"></i>
                            <div class="info">
                                <div class="head">Address</div>
                                <div class="sub-title">Surkhet, Nepal</div>
                            </div>
                        </div>
                        <div class="row">
                            <i class="fas fa-envelope"></i>
                            <div class="info">
                                <div class="head">Email</div>
                                <div class="sub-title">abc@gmail.com</div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="column right">
                    <div class="text">Message me</div>
                    <form action="#">
                        <div class="fields">
                            <div class="field name">
                                <input type="text" placeholder="Name" required>
                            </div>
                            <div class="field email">
                                <input type="email" placeholder="Email" required>
                            </div>
                        </div>
                        <div class="field">
                            <input type="text" placeholder="Subject" required>
                        </div>
                        <div class="field textarea">
                            <textarea cols="30" rows="10" placeholder="Message.." required></textarea>
                        </div>
                        <div class="button-area">
                            <button type="submit">Send message</button>
                        </div>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- footer section start -->
    <footer>
        <span>Created By <a href="https://www.codingnepalweb.com">CodingNepal</a> | <span class="far fa-copyright"></span> 2020 All rights reserved.</span>
    </footer>

    <script src="script.js"></script>
</body>
</html>
<script>
  $(document).ready(function(){
    $(window).scroll(function(){
        // sticky navbar on scroll script
        if(this.scrollY > 20){
            $('.navbar').addClass("sticky");
        }else{
            $('.navbar').removeClass("sticky");
        }
        
        // scroll-up button show/hide script
        if(this.scrollY > 500){
            $('.scroll-up-btn').addClass("show");
        }else{
            $('.scroll-up-btn').removeClass("show");
        }
    });

    // slide-up script
    $('.scroll-up-btn').click(function(){
        $('html').animate({scrollTop: 0});
        // removing smooth scroll on slide-up button click
        $('html').css("scrollBehavior", "auto");
    });

    $('.navbar .menu li a').click(function(){
        // applying again smooth scroll on menu items click
        $('html').css("scrollBehavior", "smooth");
    });

    // toggle menu/navbar script
    $('.menu-btn').click(function(){
        $('.navbar .menu').toggleClass("active");
        $('.menu-btn i').toggleClass("active");
    });

    // typing text animation script
    var typed = new Typed(".typing", {
        strings: ["YouTuber", "Developer", "Blogger", "Designer", "Freelancer"],
        typeSpeed: 100,
        backSpeed: 60,
        loop: true
    });

    var typed = new Typed(".typing-2", {
        strings: ["YouTuber", "Developer", "Blogger", "Designer", "Freelancer"],
        typeSpeed: 100,
        backSpeed: 60,
        loop: true
    });

    // owl carousel script
    $('.carousel').owlCarousel({
        margin: 20,
        loop: true,
        autoplay: true,
        autoplayTimeOut: 2000,
        autoplayHoverPause: true,
        responsive: {
            0:{
                items: 1,
                nav: false
            },
            600:{
                items: 2,
                nav: false
            },
            1000:{
                items: 3,
                nav: false
            }
        }
    });
});
</script>
