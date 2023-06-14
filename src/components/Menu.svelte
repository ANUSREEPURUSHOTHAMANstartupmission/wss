  
 <section class="bg-black px-10 py-2 flex justify-between border-b border-white shadow">
	<div class="flex justify-between items-center w-full">
	  <div class="flex items-center">
		<img src="/img/logo-white.svg"  alt="" class="h-14">
		<a href="https://startupmission.kerala.gov.in" target="_blank" class="inline-block ml-4 pl-4 text-white text-lg py-3 border-l-2">
		  Connect with Us
		</a>
	  </div>
  
	  <div class="hidden md:flex">
		<div class="relative inline-block text-left z-10">
			<!-- <a href="/wss/wespark" class="inline-flex justify-center w-full text-white hover:bg-slate-900  px-5 py-3 text-sm font-medium " id="menu-button" aria-expanded="true" aria-haspopup="true">
			  We Spark
			</a> -->
		</div>
		<div class="relative inline-block text-left z-10">
			<a href="/wss/" class="inline-flex justify-center w-full text-white hover:bg-slate-900  px-5 py-3 text-sm font-medium " id="menu-button" aria-expanded="true" aria-haspopup="true">
			  Home
			</a>
		</div>
		<div class="group relative inline-block text-left z-10">
		  <div class=" ">
			<div  class="inline-flex justify-center w-full text-white hover:bg-slate-900  px-5 py-3 text-sm font-medium " id="menu-button" aria-expanded="true" aria-haspopup="true">
			  Previous Edition
			</div>
		  </div>
		  <div class=" absolute hidden group-hover:block text-left z-10 w-56 bg-black ">
			<div class="">
			  <a   href="/wss/2022_women_startup_summit" class="inline-flex justify-center w-full text-white  px-5 py-3 text-sm font-medium " id="menu-button" aria-expanded="true" aria-haspopup="true">
				Women Startup Summit 2022
			  </a>
			</div>
			<div class="">
				<a target="_blank" href="https://2021.womenstartupsummit.com" class="inline-flex justify-center w-full text-white  px-5 py-3 text-sm font-medium " id="menu-button" aria-expanded="true" aria-haspopup="true">
				  Women Startup Summit 2021
				</a>
			  </div>
		  </div>
		</div>
		<div class="group relative inline-block text-left z-10">
			<div class=" ">
			  <div  class="inline-flex justify-center w-full text-white hover:bg-slate-900  px-5 py-3 text-sm font-medium " id="menu-button" aria-expanded="true" aria-haspopup="true">
				Shelovestech
			  </div>
			</div>
			<div class=" absolute hidden group-hover:block text-left z-10 w-56 bg-black md:-right-9">
			  <div class="">
				<a target="_blank"  href="/wss/shelovestech" class="inline-flex  justify-center w-full text-white  px-5 py-3 text-sm font-medium " id="menu-button" aria-expanded="true" aria-haspopup="true">
					Shelovestech 2023
				</a>
			  </div>
			  <div class="">
				  <a target="_blank"  href="/wss/shelovestech2022" class="inline-flex justify-center w-full text-white  px-5 py-3 text-sm font-medium " id="menu-button" aria-expanded="true" aria-haspopup="true">
					Shelovestech 2022
				  </a>
				</div>
			</div>
		  </div>
		
	  </div>
  
	  <button on:click="{()=> menu_open = !menu_open }" class="cursor-pointer fixed right-5 w-10 h-10 text-xl ml-auto transition duration-150 hover:shadow leading-none px-2 py-1 border border-solid border-transparent rounded bg-transparent block lg:hidden outline-none focus:outline-none" type="button">
		<span class="block absolute w-6 h-0.5 rounded-sm bg-gray-600 top-3 duration-500 { menu_open ? 'opacity-0':'' }" ></span>
		<span class="block absolute w-6 h-0.5 rounded-sm bg-gray-600 duration-500 { menu_open ? 'transform rotate-45':'' }"></span>
		<span class="block absolute w-6 h-0.5 rounded-sm bg-gray-600 duration-500 { menu_open ? 'transform -rotate-45':'' }"></span>
		<span class="block absolute w-6 h-0.5 rounded-sm bg-gray-600 bottom-2.5 duration-500 { menu_open ? 'opacity-0':'' }"></span>
	  </button>
	</div>
	<div>
  
	</div>
  </section>


  
  <script is:inline>
	
  
	let menu_open = false;
  
	let menu_slt = [
	  {
		"label" : "2021",
		"link" : "https://startupmission.in/shelovestech/2021.html",
		"target" : "_blank"
	  },
	  {
		"label" : "2020",
		"link" : "https://startupmission.in/shelovestech/2020.html",
		"target" : "_blank"
	  },
	  {
		"label" : "2019",
		"link" : "https://startupmission.in/shelovestech/2019.html",
		"target" : "_blank"
	  }
	];
  
	let menu_wss = [
	  {
		"label" : "2020",
		"link" : "https://startupmission.in/womensummit/2020/",
		"target" : "_blank"
	  },
	  {
		"label" : "2019",
		"link" : "https://startupmission.in/womensummit/2019/",
		"target" : "_blank"
	  }
	]
  
	let videoId = "3D41jkThUbQ";
	let player;
	let open = false;
  
	let national_partners = [
	  {
		"image" : "startupindia.png"
	  },
	];
  
	let media_partners = [
	  {
		"image" : "herstart.png"
	  },
	];
  
	let eco_partners = [
	  
	  {
		"image" : "aws.png"
	  },
	  {
		"image" : "google.png"
	  },
	  {
		"image" : "ey.png"
	  },
	  {
		"image" : "fitt.png"
	  },
	  {
		"image" : "cii.png"
	  },
	  {
		"image" : "encubay.png"
	  },
	  {
		"image" : "kma.png"
	  },
	  {
		"image" : "msmf.png"
	  },
	  {
		"image" : "tiew.png"
	  },
	  {
		"image" : "nsrcel.png"
	  },
	  {
		"image" : "tsic.png"
	  },
	  {
		"image" : "thub.png"
	  },
	  {
		"image" : "10000.png"
	  },
	  {
		"image" : "headstart.png"
	  },
	  {
		"image" : "ciie.png"
	  },
	  {
		"image" : "wien.png"
	  },
	  {
		"image" : "wicci.png"
	  },
	  {
		"image" : "riidl.png"
	  },
	  {
		"image" : "flex.png"
	  },
	  {
		"image" : "ourea.png"
	  },
	  {
		"image" : "hermoney.png"
	  }
	];
  </script>