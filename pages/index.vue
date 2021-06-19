<template>
  <div>
	<head>
        <meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
    </head>
    <body>Verification: fcd149470bcd86c1</body>
    <div class="carlogo"><img src="@/static/background.png"/></div>
		<p class="htext">Преимущества Ferrari</p>
			<div class="card mb-3" style="max-width:100%">
  				<div class="row no-gutters">
    				<div class="col-md-4">
      					<img src="@/static/k2.jpg" class="card-img">
    				</div>
    				<div class="col-md-8">
      					<div class="card-body">
						<img src="@/static/legend.png" class="iconim">
        				<h5 class="card-title">Легендарный автопром</h5>
        				<p class="card-text">Ferrari - однин из первых автомобильных концернов завоевавших уважение и доверие всего мира ценителей автомобилестроения.</p>
      					</div>
    				</div>
  				</div>	
  			</div>

			<div class="card mb-3" style="max-width:100%">
  				<div class="row no-gutters">
    				<div class="col-md-8">
      					<div class="card-body">
						<img src="@/static/speed.png" class="iconim">
        				<h5 class="card-title">Высокая скорость</h5>
        				<p class="card-text">Ferrari - это в первую очередь спортивный автомобиль, его динамика сможет впечатлить любого водителя </p>
      					</div>
    				</div>
					<div class="col-md-4">
      					<img src="@/static/k3.jpg" class="card-img">
    				</div>
  				</div>	
  			</div>

			<div class="card mb-3" style="max-width:100%">
  				<div class="row no-gutters">
    				<div class="col-md-4">
      					<img src="@/static/k1.jpg" class="card-img">
    				</div>
    				<div class="col-md-8">
      					<div class="card-body">
						<img src="@/static/acseler.png" class="iconim">
        				<h5 class="card-title">Отличная управляемость</h5>
        				<p class="card-text">Благодаря лучшим инженерам любой автомобиль Ferrari имеет идеальную управляемость</p>
      					</div>
    				</div>
  				</div>	
  			</div>
		
		<p class="htext">Широкий модельный ряд</p>
			
			<div id="carouselExampleIndicators" class="carousel slide" data-ride="carousel">
  				<ol class="carousel-indicators">
    				<li data-target="#carouselExampleIndicators" data-slide-to="0" class="active"></li>
    				<li data-target="#carouselExampleIndicators" data-slide-to="1"></li>
    				<li data-target="#carouselExampleIndicators" data-slide-to="2"></li>
  				</ol>
  				<div class="carousel-inner">
    				<div class="carousel-item active">
      					<img src="https://www.tokkoro.com/picsup/2817254-car-ferrari-ferrari-458-red-cars___cars-wallpapers.jpg" class="d-block w-100" >
    				</div>
    				<div class="carousel-item">
      					<img src="https://www.nastol.com.ua/download.php?img=201401/1920x1080/nastol.com.ua-83072.jpg" class="d-block w-100" >
    				</div>
					<div class="carousel-item">
						<img src="https://www.nastol.com.ua/download.php?img=201912/1920x1080/nastol.com.ua-373787.jpg" class="d-block w-100">
					</div>
  				</div>
			</div>
    			<div v-if="isMounted">
      				<yandex-map :coords="[55.758904,37.623609]" zoom="10" class="map">
        				<ymap-marker markerId="1" marker-type="placemark" hint-content="element.hint" :coords="[55.758904,37.623609]"></ymap-marker>
						<ymap-marker markerId="2" marker-type="placemark" hint-content="element.hint" :coords="[55.741683,37.298608]"></ymap-marker>
						<ymap-marker markerId="3" marker-type="placemark" hint-content="element.hint" :coords="[55.738247,37.262819]"></ymap-marker>
      				</yandex-map>
    			</div>
  </div>
</template>

<script>
import Vue from 'vue'

export default {
  data: () => ({
    isMounted: false
  }),
  mounted() {
    this.isMounted = true;
  }
}
</script>

<style>
*{
	margin:0;
	padding:0;
}
@font-face {
    font-family:'Montserrat';
    src: url("fonts/Montserrat-Regular.ttf") format("truetype");
    font-style: normal;
    font-weight: normal;
  }
body{
	font-family:Montserrat,sans-serif;
	background-repeat:no-repeat;
	background-color:black;
}
.htext{
	font-size: 8vh;
	color:white;
	border-bottom:0.2vh solid #890000;
	margin:0 auto;
	text-align:center;
}
.carlogo{
	width:100%;
}
.carlogo>img{
	width:100%;
}
.icons{
	width:30vh;
}
.icdiv{
	height:30vh;
	text-align:center;
}
.conttext{
	color:white;
	font-size:3vh;
	text-align:center;
	width:35vh;
}
.carousel{
	width:95%;
	margin:2vh auto;
}
.card{
	background-color: black;
	width:95%;
	border:0.5vh solid #890000;
	opacity: 0.7;
	transition:0.5s;
	margin:0 auto;
	margin-top:5vh;
}
.card:hover{
	opacity: 1;
}
.card-title{
	color:white;
}
.card-text{
	color:white;
}
.col-md-8{
	text-align: center;
}
.iconim{
	width:10vh;
}
.ymap-container {
  height: 800px;
}
  @media (max-width:600px){
  .ymap-container{
	  height: 300px;
  }
  }
</style>
