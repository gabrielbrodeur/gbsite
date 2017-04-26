# gbsite
<!doctype html>
<html>

<head>
<meta charset="utf-8">
<title>Gabriel Brodeur</title>
<link href="GabrielBrodeurCSS.css" rel="stylesheet" type="text/css">
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.0/jquery.min.js"></script>
<link rel="stylesheet" href="https://ajax.googleapis.com/ajax/libs/jqueryui/1.12.1/themes/smoothness/jquery-ui.css">
<script src="https://ajax.googleapis.com/ajax/libs/jqueryui/1.12.1/jquery-ui.min.js"></script>
<link href="https://fonts.googleapis.com/css?family=Open+Sans|Open+Sans+Condensed:300|Roboto|Ubuntu" rel="stylesheet">
</head>

<body>	

<div id="header">	
	<header class="nav-down">
		<div class="logo">
			<h1>Gabriel Brodeur</h1>
			<h2>Freelance webdev and digital marketing</h2>
		</div>
		
        <div class="menu">
			<ul class="menu_list">
				<li class="menu_button">Resume</li>
				<li class="menu_button">About</li>
				<li class="menu_button">Blog</li>
				<li class ="button">Let's chat</li>
			</ul>
		</div>
	</header>	
</div>

<div class="wrapper">
<div class="source">
	<div class="CTA">
		 <h2> Affordable digital freelancer</h2>
		 <h3> Suck it</h3>
        <p class="button" id="CTA_button_size"><strong>Buy from me</strong></p>
    </div>
	<div class="video_container">
		<video>
			<source src="backgroundvid.mp4">
		</video>
	</div>
  <div class="background"></div>
</div>
</div>
<div class="second_fold">
	<div class="img_slider">
		<ul class="referrals">	
			<li><img src="Bob Kendrick.jpg" class="bob_kendrick">
        
            <li>
			<li><img src="Dustin Img.jpg" class="dustin_mena">
        
            </li>
			<li><img src="Rosie Img.jpg" class="rosie_maturan">
        
            </li>
			<li><img src="Tia Small.jpg" class="tia_small">
        
            
            </li>
		</ul>
	</div>	
</div>

<div class ="third_fold">
	<div class="skills">
		<ul>
            <div class="skills-tabs"><li>Digital Marketing</li></div>
            <div class="skills-tabs"><li>Web Development</li></div>
            <div class="skills-tabs"><li>Product Launch</li></div>
            <div class="skills-tabs"><li>Social Media Management</li></div>

        </ul>
	</div>
	<div class="skills_links">
	</div>
	
</div>

</body>

<script>
	
// Header fader
var didScroll;
var lastScrollTop = 0;
var delta = 3;
var navbarHeight = $('header').outerHeight();

$(window).scroll(function(event){
    didScroll = true;
});

setInterval(function() {
    if (didScroll) {
        hasScrolled();
        didScroll = false;
    }
}, 250);

function hasScrolled() {
    var st = $(this).scrollTop();
    
    // Make sure they scroll more than delta
    if(Math.abs(lastScrollTop - st) <= delta)
        return;
    
    // If they scrolled down and are past the navbar, add class .nav-up.
    // This is necessary so you never see what is "behind" the navbar.
    if (st > lastScrollTop && st > navbarHeight){
        // Scroll Down
        $('header').removeClass('nav-down').addClass('nav-up');
    } else {
        // Scroll Up
        if(st + $(window).height() < $(document).height()) {
            $('header').removeClass('nav-up').addClass('nav-down');
        }
    }
    
    lastScrollTop = st;
}
	
 
// carousel 

	
</script>

</html>

@charset "utf-8";
/* CSS Document */

.nav-down {
    height: 50px;
    width: 100%;
    background-color: transparent;
    position: fixed;
    z-index: 1000;
}

.nav-up {
    top: -40px;
}

.logo {
	float: left;
	margin-left: .5em;
	font-family: Open+Sans; 
	color: white;
}


.logo h2 {
	margin-top: -1em;
	margin-left: 1em;
	font-family: Open+Sans+Condensed:300;
}


.background {
	opacity: 0.5;
	background-image: linear-gradient(-226deg, #29506d 0%, #1768a7 100%);
	position: absolute;
	z-index: 100;
	width: 100%;
	height: 60em;
	top: 0;
	left: 0;
	margin: auto;
}

.video_container {
	opacity: 0.7;
	position:absolute;
	top: 0;
	bottom: 0;
	width: 100%; 
	height: 69em;
	overflow: hidden;
	overflow-x:hidden;
	overflow-y:hidden;
    margin-top: -8em;
    margin-left: -.5em
}

.video_container video {
	min-width: 100%;
	min-height: 100%;
	width: 100%;
	height: 100%;
	top: 50%;
	bottom:50%;
	object-fit: contain;
}

.source{
    
    height: 25em;
	width: 100%;
	
}

.CTA {
	margin-top: 25em;
	margin-left: 20em;
	position: absolute;
	z-index: 500;
	width: 40em;
    height: 10em;
	padding-right: 0px;
}

.CTA h2 {
	font-family: Open+Sans;
	font-size: 3em;
}

.CTA h3 {
	font-family: Roboto;
	font-size: 2em;
}

.CTA p {
    font-family: Open+Sans;
    font-size: 20px; 
    text-align: center;
}

#CTA_button_size {
    width: 7em;
    margin-right: 0px;
}
.button {
    opacity: 1.0;
    transition: opacity 0.2s;
    margin-top: -15px;
	padding: 15px 32px;
	text-decoration: none;
	color:white;
	border-radius: 25px;
    width:auto;
    background: linear-gradient(to bottom, rgba(57,204,204,1) 0%, rgba(34,122,122,1) 100%);
   
}

.button:hover {
    opacity: 0.5;
}
    


.menu {
	float: right;
	z-index: 1000;
    
}


ul.menu_list {
	color: white;
	list-style: none;
	display: flex;
	font-family: sans-serif;
	margin-top:3em;
}


ul.menu_list li {
	margin-right: 2em;
}

.menu_button:hover {
    text-decoration: underline;
    text-shadow: 2px;
}


.second_fold {
    margin-top: 25em;
	height: 25em;
	margin:none;	
	width:100%;
	top: 0;
	bottom: 0;
    background: linear-gradient(to bottom, rgba(57,204,204,1) 50%, rgba(34,122,122,1) 100%);
    
}

.img_slider {
    margin-top: 34.5em;
	width: 720px;
	height: 400px;
	overflow: hidden;
}

.referrals {
	list-style: none;
	display: block;
	width:6000px;
	height: 400px;
	margin: 0;
	padding: 0;
}

.referrals img {
	float: left;
	height: 20em;
	width: 20em;
	border-top-left-radius: 5em;
	border-bottom-left-radius: 5em;
    margin-top: 2.5em;
    
}

.third-fold {
    background-color:lightgray; 
}

.skills {
	float: left;
	border: 1px solid black;
	width: 450px;
	height: 800px;
	margin-left: 50px;
	margin-top: 250px;
}


.skills_links {
	float: right;
	border: 1px solid black;
	width: 950px;
	height: 800px;
	margin-top: 300px;
	margin-right: 50px;
}

.skills-tabs {
    width: 400px;   
    height: 200px; 
    border: solid black .5px; 
    margin-left: -2em; 
    background-image:linear-gradient(-226deg, #c6c6c6, #778899);
    opacity: 50%; 
    margin-top: 5px; 
    
    
}

.skills-tabs li {
    list-style-type: none; 
    text-align: center; 
    font-size: 38px; 
    padding: 90px 0; 
    font-family: Open+Sans;
}

.skills-tabs:hover {
    opacity: 50%; 
}
