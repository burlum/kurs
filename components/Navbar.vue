<template>
<div>
	  	<script src="https://code.jquery.com/jquery-3.5.1.slim.min.js" integrity="sha384-DfXdz2htPH0lsSSs5nCTpuj/zy4C+OGpamoFVy38MVBnE+IbbVYUew+OrCXaRkfj" crossorigin="anonymous"></script>
		<script src="https://cdn.jsdelivr.net/npm/popper.js@1.16.1/dist/umd/popper.min.js" integrity="sha384-9/reFTGAW83EW2RDu2S0VKaIzap3H66lZH81PoYlFhbGU+6BZp6G7niu735Sk7lN" crossorigin="anonymous"></script>
		<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js" integrity="sha384-B4gt1jrGC7Jh4AgTPSdUtOBvfO8shuf57BaghqFfPlYxofvL8/KUEfYiJOMMV+rV" crossorigin="anonymous"></script>
		
    <nav class="navbar navbar-expand-lg">
		  <a class="navbar-brand" href="#"><img class="logo" src="@/static/logo.png"><img></a>
		  <div class="collapse navbar-collapse" id="navbarNavDropdown">
			<ul class="navbar-nav">
			  <li class="nav-item">
				<nuxt-link class="nav-link" to="/">Главная <span class="sr-only">(current)</span></nuxt-link>
			  </li>
			  <li class="nav-item">
				<nuxt-link class="nav-link" to="/katalog">Каталог</nuxt-link>
			  </li>
			  <li class="nav-item">
				<nuxt-link class="nav-link" to="/about">О нас</nuxt-link>
			  </li>
			</ul>
		  </div>
		</nav>
</div>
</template>


<style>
nav{
	background-color:#890000;
    height:10vh;
	margin-top:5vh;
	position:absolute;
	z-index:9;
}
.logo{
	width:20vh;
}
.nav-link{
	color:white;
	transition: 0.5s;
}
.nav-link:hover{
	color:gray;
}
  @media (max-width:600px){
	  nav{
		  font-size: 50%;
	  }
	  .logo{
		  margin-top:-7vh;
	  }
    }
</style>