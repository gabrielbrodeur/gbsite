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
