# Coronavirusdataset
<!DOCTYPE html>
<html>
<head>
	<title>Scrollytelling template</title>
	<script src="https://unpkg.com/enter-view"></script>
</head>
<style type="text/css">
body, html {
	font-family:"Helvetica-Neue", sans-serif;
	top:0;
	left:0;
	margin:0;
	color:#1d1d1d;
}
#featured {
  display:flex;
  justify-content:center;
  align-items:center;
  width:100%;
  overflow:none;
}
.aligner {
	max-width:80%;
}
#featured .title{
	text-align:center;
	margin-top:5%;
	width:100%;
}
.title h2 {
	font-size:1em;
	font-weight:400;
}
#featured img {
  width:100%;
}
#scroll {
  font-stretch:expanded;
  text-align:center;
  width:80%;
  position:absolute;
  bottom:10%;
  font-size:6em;
  color:#1d1d1d;
  cursor:pointer;
  transition:0.5s all ease-in-out;
  line-height:0.5em;
}
#scroll:hover {
  transform:scale(1.2);
  transform-origin:50% 30%;
}
.section{
  opacity:0;
  width:90%;
  height:auto;
  padding:5%;
  margin-bottom:0%;
  padding-bottom:0%;
  line-height:2em;
  transform:translateY(5em);
  transition:0.5s ease-in-out;
  margin:auto;
}
.section img {
	width:100%;
}
.entered {
  transform:translateY(0em);
  opacity:1;
}
.tableauPlaceholder {
	height:50vh;
}
.scrollpost {
	width:100%;
	padding:0;
	margin:0;
	overflow-x:scroll;
	overflow-y:hidden;
	white-space:nowrap;
}
.scrollpost img {
	width:25%;
	display:inline-block;
	margin:0% 4% 0% 0%;
}
.open {
	position:relative;
		text-align:center;
	margin:auto;
}
.open:hover .overlay{
	opacity:0.8;
}
.overlay {
	position: absolute;
	top: 0;
	bottom: 0;
	left: 0;
	right: 0;
	height: 100%;
	width: 100%;
	background-color: black;
	opacity:0;
	display:flex;
	justify-content: center;
	align-items: center;
	cursor:pointer;
	transition:0.5s ease-in-out;
}
.open img {
	width:80%;
}

.overlay h2 {
	color:white;
	background-color:none;
	margin:auto;
}
#final {
	margin-bottom:5%;
}
.open a {
	text-decoration:none;
	background-color:none;
	padding:2% 4%;
	cursor:pointer;
	border:0.05em solid white;
	transition:0.5s ease-in-out;
}
.open a:hover {
	background-color:white;
}
.open a:hover h2{
	color:#1d1d1d;
}
@media screen and (max-width:767px){
	#featured img {
		margin-left:-50%;
		bottom:0;
		position:absolute;
		width:200%;
		z-index:0;
	}
	#featured .title {
		z-index:1;
	}
	.scrollpost img {
		width:70%;
	}
}
</style>
<body>

<div id="featured">
	<div class="aligner">
		<div class="title">
		<h1>Coronavirus Data Set</h1>
		<h2>Vanessa Nefve</h2>
		</div>
	  	<img src="assets/featured/cover.png">
	 	 <div id="scroll">&#xfe40;</div>	
	</div>
</div>

<!-- Simple text intro -->
<div class="section" id="first">
	<h1>About the project</h1>
	<p>I wanted to explore the way that coronavirus effects different demographics. It is incredibly important to note that the virus has disporportionately effected black and brown communities. Long-standing systemic health and social inequities have put many people from racial and ethnic minority groups at increased risk of getting sick and dying from COVID-19.People from some racial and ethnic minority groups are disproportionately represented in essential work settings such as healthcare facilities, farms, factories, grocery stores, and public transportation. As all data has proven people who are older have a much higher chance of dying from the virus. </p>
</div>
	<div class="scrollpost">
</div>
		<div/> 
		<img src="assets/about-the-data/7.gif">
<!-- About the data carousel -->
<div class="section">
	<h1>About the data</h1>
	<p>The data was collected from the Center for Disease Control, it contained infromation about United states Coronavirus data. It includes data about race, sex, age, hospitalized patients, and ICU patients.</p>
		<div/> 
	<!-- the scrolling post holder -->
	<div class="scrollpost">
		<img src="assets/about-the-data/1.png">
		<img src="assets/about-the-data/2.png">
		<img src="assets/about-the-data/3.png">
	</div>

</div>
		<div/> 
			<div/> 

<div class="section">
	<h1>Cases by Race</h1>
	<img src="assets/casestudy/image.png">
</div>
<!-- Tableau Public embed -->

<div class="section">
</div>

<!-- About the data carousel -->
<div class="section">
	<h1>Hospitalizations and ICU Cases</h1>
	<!-- the scrolling post holder -->
	<div class="scrollpost">
		<img src="assets/months/jan.png">
		<img src="assets/months/feb.png">
	</div>

		</div>
		<img src="assets/source/asource.gif">

<div class="section" id=final>
		<div class='open'>
			<div class='overlay'>
				<a href="assets/interactive/index.html" target="_blank">
					<h2>View</h2>
				</a>
			</div>
		</div>
</div>


</body>
<script type="text/javascript">

scroll=document.querySelector('#scroll');
setup = document.querySelector('#first');
scroll.onclick=function() {
    first.scrollIntoView({ 
    behavior: 'smooth',
    block: "start",
  });
};

enterView({
  selector: '.section',
  enter: function(el) {
    el.classList.add('entered');
  },
  exit: function(el) {
    el.classList.remove('entered');
  },
  progress: function(el, progress) {

  },
  offset: 0.2, // enter at middle of viewport
});

</script>
</html>
