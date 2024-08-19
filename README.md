# Portfoilo
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="./css/font-awesome.css">
    <link rel="stylesheet" href="">
    <style>
        * {
            margin: 0px;
            padding: 0px;
            font-family: Arial, Helvetica, sans-serif;
            box-sizing: border-box;
        }

        body {
            background: #080808;
            color: #fff;

        }

        #header {
            width: 100%;
            height: 100vh;
            background-image: url("./dev.png");
            background-size: cover;
            background-position: center;
        }

        .container {
            padding: 10px 10%;
        }

        nav {
            display: flex;
            align-items: center;
            justify-content: space-between;
            flex-wrap: wrap;
        }

        .logo {
            width: 140px;
        }

        nav ul li {
            display: inline-block;
            list-style: none;
            margin: 10px 20px;
            position: relative;
        }

        nav ul li a {
            color: #fff;
            text-decoration: none;
            font-size: 18px;
        }

        nav ul li a::after {
            content: '';
            width: 0;
            height: 3px;
            background: #ff004f;
            position: absolute;
            left: 0;
            bottom: -6px;
            transition: 0.5s;

        }

        nav ul li a :hover::after {
            width: 100%;

        }

        .header-text {
            margin-top: 20%;
            font-size: 30px;
        }

        .header-text h1 {
            font-size: 60px;
            margin-top: 30px;
        }

        .header-text h1 span {
            color: #ff004f;
        }

        /* ABOUT */
        #about {
            padding: 80px 0px;
            color: #ababab;
        }

        .row {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
        }

        .about-col-1 {
            flex-basis: 35%;
        }

        .about-col-1 img {
            width: 100%;
            border-radius: 15px;
        }

        .about-col-2 {
            flex-basis: 60%;
        }

        .sub-title {
            font-size: 60px;
            font-weight: 600;
            color: #fff;
        }

        .tab-titles {
            display: flex;
            margin: 20px 0px 40px;
        }

        .tab-links {
            margin-right: 50px;
            cursor: pointer;
            font-size: 18px;
            font-weight: 500;
            position: relative;
        }

        .tab-links::after {
            content: '';
            width: 0;
            height: 3px;
            background: #ff004f;
            position: absolute;
            left: 0;
            bottom: -8px;
            transition: 0.5s;
        }

        .tab-links.active-link::after {
            width: 50%;
        }

        .tab-contents ul li {
            margin: 10px 0;
            list-style: none;
        }

        .tab-contents ul li span {
            color: #b54769;
            font-size: 14px;
        }

        .tab-contents {
            display: none;
        }

        .tab-contents.active-tab {
            display: block;
        }

        /* project */
        #project {
            padding: 30px 0;
        }

        .project-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            grid-gap: 40px;
            margin-top: 50px;
        }

        .project-list div{
            background: #262626;
            padding: 40px;
            font-weight: 300;
            font-size: 13px;
            border-radius: 10px;
            transition:background 0.5s,transform 0.5s ;
        }
        .project-list div h2{
            font-size: 25px;
            font-weight: 500;
            margin-bottom: 15px;
        }
        .project-list div a{
            text-decoration: none;
            color: #fff;
            font-size: 12px;
            margin-top: 20px;
        }

        /* portfolio */
        #Portfolio {
            padding: 50px 0;
        }

        .work-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            grid-gap: 40px;
            margin-top: 50px;
        }

        .work {
            border-radius: 10px;
            position: relative;
            overflow: hidden;
        }

        .work img {
            width: 100%;
            border-radius: 10px;
            display: block;
            transition: transform 0.5s;
        }
        .layer{
            width: 100%;
            height: 0;
            background: linear-gradient(rgba(0,0,0,0.6),#ff004f);
            border-radius: 10px;
            position: absolute;
            left: 0;
            bottom: 0;
            overflow: hidden;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-direction: column;
            padding: 0 40px;
            text-align: center;
            font-size: 14px;
            transition: height 0.5s;
        }
        .layer h3{
            font-weight: 500;
            margin-bottom: 20px;
        }
        .layer a{
            margin-top: 20px ;
            color: #ff004f;
            text-decoration: none;
            font-size: 18px;
            line-break: 60px;
            background: #fff;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            text-align: center;
        }
        .work:hover img{
            transition: scale(1.1) ;
        }
        .work:hover .layer{
            height:100% ;

        }
        .btn{
            display: block;
            margin: 50px auto;
            width: fit-content;
            border:1px solid #ff004f ;
            padding: 14px 50px;
            border-radius: 6px;
            text-decoration: none;
            color: #fff;
            transition: background 0.5s;
        }
        .btn:hover{
            background: #ff004f;
        }
        /* contact */
        .contact-left{
            flex-basis: 35%;
        }
        .contact-right{
            flex-basis: 60%;
        }
        .contact-left p{
            margin-top: 30px;
        }
        .social-icons{
            margin-top: 30px;
        }
        .social-icons a{
            text-decoration: none;
            font-size: 30px;
            margin-right: 15px;
            color: #ababab;
            display: inline-block;
            transition: transform 0.5s;
        }
    .social-icons a:hover{
        color: #ff004f;
        transform: translateY(-5px);
    }
    .btn.btn2{
        display: inline-block;
        background: #ff004f;
    }
        
    </style>
</head>

<body>
    <div id="header">
        <div class="container">
            <nav>
                <img src="" class="logo">
                <ul>
                    <li><a href="#">HOME</a></li>
                    <li><a href="#">ABOUT</a></li>
                    <!-- <li><a href="#">SERIVCES</a></li> -->
                    <li><a href="#">PORTFOLIO</a></li>
                    <li><a href="#">CONTACT</a></li>
                </ul>
            </nav>
            <div class="header-text">
                <p>FULLSTACK DEVELOPER</p>
                <h1>Hi, I'm <span> Ankita Patil </span> <br> from Islampur.</h1>
                <!-- <img src="./" alt=""> -->
            </div>
        </div>
    </div>
    <!-- ABOUT -->
    <div id="about">
        <div class="container">
            <div class="row">
                <div class="about-col-1">
                    <img src="./ANKITA.jpeg" alt="">
                </div>
                <div class="about-col-2">
                    <h1 class="sub-title">About Me</h1>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Doloremque vel aspernatur possimus
                        eligendi exercitationem voluptatem earum itaque sequi suscipit eius! Error perspiciatis commodi
                        enim minus odio repudiandae repellendus, corporis necessitatibus?</p>

                    <div class="tab-titles">
                        <p class="tab-links active-link" onclick="opentab('skills')">Skills</p>
                        <p class="tab-links" onclick="opentab('experience')">Experience</p>
                        <p class="tab-links" onclick="opentab('education')">Education</p>
                    </div>
                    <div class="tab-contents active-tab" id="skills">
                        <ul>
                            <li><span>UI/UX</span> <br>Designing Web/App interfaces</li>
                            <li><span>Web DEVELOPER</span> <br>Web app Development</li>
                            <li><span>App Development</span> <br>Buliding android/ios apps</li>
                        </ul>
                    </div>
                    <div class="tab-contents" id="experience">
                        <ul>
                            <li>Fresher</li>
                        </ul>
                    </div>
                    <div class="tab-contents" id="education">
                        <ul>
                            <li><span>2024</span> <br>BTech From Ashta</li>
                            <li><span>2020</span> <br>HSC From Islampur</li>
                            <li><span>2018</span> <br>SSC From Islampur</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <!-- my project -->
    <div class="container">
        <h1 class="sub-title">My Project</h1>
        <div class="project-list">
            <div>
                <h2>Student Attendance Monitoring System</h2>
                <p>This Project will help to track and store the attendance data in real
                    time. If student is Absent the sms will forward to his parents
                </p>
                <a href="#">Learn more</a>
            </div>

            <div>
                <h2>Implementation of field-oriented control strategy for
                    induction machine. </h2>
                <p>This project will help control the speed and torque of induction
                    machine. 
                </p>
                <a href="#">Learn more</a>
            </div>
            <div>
                <h2>Simulation of Electric Vehicle using MATLAB</h2>
                <p>The working and modeling of the electric vehicle are done with the
                    help of MATLAB software. 
                </p>
                <a href="#">Learn more</a>
            </div>

        </div>
    </div>

    <!--portfolio -->
    <div id="Portfolio">
        <div class="container">
            <h1 class="sub-title">My Work</h1>
            <div class="work-list">
                <div class="work">
                    <img src="./flip.png">
                    <div class="layer">
                        <h3>Flipcart clone</h3>
                        <p>I have Created a Flipcart clone using Html properites and giving a beautification by using Css.</p>
                        <!-- <a href="#"></a> -->
                    </div>
                </div>
                <div class="work">
                    <img src="./google.png">
                    <div class="layer">
                        <h3>Google Clone</h3>
                        <p>I have Created a Google using Html properites and giving a beautification by using Css.</p>
                        <!-- <a href="#"></a> -->
                    </div>
                </div>
                <div class="work">
                    <img src="./tribute.png">
                    <div class="layer">
                        <h3>Tribute Page</h3>
                        <p>I have Created a Tribute page on Lata Mageshkar using Html properites and giving a beautification by using Css</p>
                        <!-- <a href="#"></a> -->
                    </div>
                </div>
            </div>
            <a href="#" class="btn">See more</a>
        </div>
    </div>
    <!-- contact -->
     <div id="contact">
        <div class="container">
            <div class="row">
                <div class="contact-left">
                    <h1 class="sub-title">Contact me</h1>
                    <p>contact@example.com</p>
                    <p>9022698410</p>
                    <div class="social-icons">
                        <a href="http://www.instagram.com"><i class="fa fa-instagram"></i></a>
                        <a href="http://www.twitter.com"><i class="fa fa-twitter-square"></i></a>
                        <a href="http://www.linkdln.com"><i class="fa fa-linkdln"></i></a>
                        <a href="http://www.telegram.com"><i class="fa fa-telegram"></i></a>
                    </div>
                    <a href="cv" download class="btn btn2">Download Cv</a>
                </div>
                <div class="contact-right">
                    <form>
                        <input type="text" name="Name" placeholder="Youe Name"required > 
                        <br>
                        <br>
                        <input type="text" name="email" placeholder="Youe email"required > 
                        <br>
                        <br>
                        <textarea name="Message" id="" cols="30" rows="6" placeholder="your message"></textarea>
                        <br>
                        <br>
                      <button type="submit">submit</button>
                    </form>
                </div>
            </div>
        </div>
     </div>











    <script>
        var tablinks = document.getElementsByClassName("tab-links");
        var tabcontents = document.getElementsByClassName("tab-contents");
        function opentab(tabname) {
            for (tablink of tablinks) {
                tablink.classList.remove("active-link");
            }
            for (tabcontent of tablcontents) {
                tabcontent.classList.remove("active-tab");
            }
            event.currentTarget.classList.add("active-link");
            document.getElementById(tabname).classList.add("active-tab");
        }
    </script>
</body>

</html>
