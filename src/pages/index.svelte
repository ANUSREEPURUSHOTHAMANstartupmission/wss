<script>
  import Speakers from "../components/Speakers.svelte";
  import Partners from "../components/Partners.svelte";
  import Nav from '../components/Navbar.svelte';
  import Dropdown from "../components/Dropdown.svelte";
  import { Plyr } from "svelte-plyr";
  import Info from "../components/Info.svelte";
  import Agenda from "../components/Agenda.svelte";
  import Tracks from "../components/Tracks.svelte";

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

<section class="bg-black px-10 py-2 flex justify-between border-b border-white shadow">
  <div class="flex justify-between items-center w-full">
    <!-- <img src="/wss/img/slt-logo.png" alt="" class="h-16"> -->
    <div class="flex items-center">
      <img src="/wss/img/logo-white.svg"  alt="" class="h-14">
      <a href="https://startupmission.kerala.gov.in" target="_blank" class="inline-block ml-4 pl-4 text-white text-lg py-3 border-l-2">
        Connect with Us
      </a>
    </div>

    <div class="hidden md:flex">
      <div class="relative inline-block text-left z-10">
          <a href="/wespark" class="inline-flex justify-center w-full text-white hover:bg-slate-900  px-5 py-3 text-sm font-medium " id="menu-button" aria-expanded="true" aria-haspopup="true">
            We Spark
          </a>
      </div>
      <div class="relative inline-block text-left z-10">
        <div on:click={()=>{open = !open}}>
          <a target="_blank" href="https://2021.womenstartupsummit.com" class="inline-flex justify-center w-full text-white hover:bg-slate-900  px-5 py-3 text-sm font-medium " id="menu-button" aria-expanded="true" aria-haspopup="true">
            Previous Edition
          </a>
        </div>
      </div>
      <div class="relative inline-block text-left z-10">
        <div on:click={()=>{open = !open}}>
          <a target="_blank" href="/shelovestech" class="inline-flex justify-center w-full text-white hover:bg-slate-900  px-5 py-3 text-sm font-medium " id="menu-button" aria-expanded="true" aria-haspopup="true">
            Shelovestech
          </a>
        </div>
      </div>
      <!-- <Dropdown title="Previous Editions" items={menu_wss} />
      <Dropdown title="SheLovesTech Inda" items={menu_slt} /> -->
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

<section class="py-24 px-5 flex items-center relative main-section">
  <div class="absolute -z-10 w-full h-full top-0 left-0 bg-black bg-opacity-70"></div>
  <div class="absolute -z-20 bg-cover bg-center bg-no-repeat w-full h-full top-0 left-0" style="background-image:url('/wss/img/wss-bg.jpg')"></div>  
  <div class="container mx-auto text-white space-y-3 md:px-10">
    
    <img src="/wss/img/wss4-white.png" alt="logo" class="h-32 -ml-5">
    <div class="font-other text-red-500 text-2xl">#WomenInAction</div>
    <div class="font-heading text-5xl md:text-6xl font-black">
      Women Startup Summit
    </div>
    <div>
      <div class="text-xl mb-2">23 September 2022 @ Kerala Technology Innovation Zone, Kochi</div>
      <div class="text-xl mb-16">24 September 2022 @ Kochi Marriot</div>
    </div>
    <div class="space-y-4 md:space-x-4 md:max-w-4xl">
      
      <button onclick="popup('women-startup-summit-40-002133');" class="font-other px-10 py-4 bg-red-600 hover:bg-red-500 inline-block">Book Tickets</button>
      
      

      <!-- <a href="/wespark" class="font-other px-10 py-5 bg-red-600 hover:bg-red-500 inline-block">We Spark</a> -->
      <!-- <a href="/kwins" class="font-other px-10 py-5 bg-red-600 hover:bg-red-500 inline-block">K-WINS</a> -->
      <!-- <a target="_blank" href="https://forms.zohopublic.com/keralastartupmission/form/Newsletter/formperma/rGJ1ZL0uSMkQ7EYwPO16hUvD7vkTB1CMd_AaPSUk9Xw" class="font-other px-10 py-5 bg-red-600 hover:bg-red-500 text-white md:hidden inline-block">Signup for Updates</a> -->
    </div>

  </div>

<!---
  <div class="fixed w-48 h-48 right-4 bottom-4 text-center text-white bg-red-600 z-30 rounded-full border-2 flex flex-col items-center justify-center">
    <div class="text-2xl font-bold">Early Bird Offer</div>
    <div class="text-md text-black">Use Code:</div>
    <div class="text-md text-black font-bold">EARLYBIRD50</div>
  </div>
  --->
</section>

<Nav bind:menu_open={menu_open} />

<section class="py-24 px-5">
  <div class="container mx-auto flex md:flex-row flex-col justify-evenly items-center">
    <div class="md:w-1/2 w-full">

      <!-- <div class="font-heading text-3xl font-bold mb-20">WSS 2022</div>
      <div class="font-other text-red-500 text-2xl">#WomenInAction</div> -->

      <Plyr bind:player={player}>
        <div class="plyr__video-embed">
          <iframe title="player"
            src="https://www.youtube.com/embed/{videoId}?iv_load_policy=3&modestbranding=1&playsinline=1&showinfo=0&rel=0&enablejsapi=1"
            allowfullscreen allowtransparency allow="autoplay">
          </iframe>
        </div>
      </Plyr>

    </div>
    <div class="md:w-1/3 w-full">
      <div class="font-heading text-3xl font-bold mb-5 mt-5 md:mt-0">WSS 2022</div>
      <div class="font-other text-red-500 text-2xl mb-5">#WomenInAction</div>
      <div class="text-xl">The 2022 Women Startup Summit will accelerate & empower the women entrepreneurs in the startup ecosystem with technology & innovation.It will give the oppurtunity to upskill and collaborate globally.The Summit will convene Women leaders in real action from all across the globe.</div>
    </div>

  </div>

  <div class="container mx-auto mt-20 text-white">

    <div class="font-other font-bold text-4xl text-center mb-10 text-red-600">Register for Parallel Tracks</div>

    <div class="grid gap-5 md:grid-cols-3 mb-5 max-w-5xl mx-auto">
      <div class="bg-red-600 text-white p-2">
        <div class="border-4 border-white h-full shadow-md p-4 text-center flex flex-col justify-between">
          <div>
            <div class="font-bold text-xl mb-3">Design Thinking Workshop</div>
            <div class="">
              Learn cognitive, strategic and practical procedures through design thinking & other aspects
            </div>
          </div>
          <button onclick="popup('women-startup-summit-40-workshop-323431');" class="p-1 inline-block mx-auto bg-white text-red-700 shadow-md mt-5">
            <div class="border-4 border-red-600 shadow-md px-8 py-2">
              Register Now
            </div>
          </button>
        </div>
      </div>
      <div class="bg-red-600 text-white p-2">
        <div class="border-4 border-white h-full shadow-md p-4 text-center flex flex-col justify-between">
          <div>
            <div class="font-bold text-xl mb-3">Fab for Women</div>
            <div class="">
              Get an insight into the world of 3 D printing and 3 D designing. Anyone with basic knowledge of computer operations & aptitude in designing can join.
            </div>
          </div>
          <button onclick="popup('women-startup-summit-40-workshop-323431');" class="p-1 inline-block mx-auto bg-white text-red-700 shadow-md mt-5">
            <div class="border-4 border-red-600 shadow-md px-8 py-2">
              Register Now
            </div>
          </button>
        </div>
      </div>
      <div class="bg-red-600 text-white p-2">
        <div class="border-4 border-white h-full shadow-md p-4 text-center flex flex-col justify-between">
          <div>
            <div class="font-bold text-xl mb-3">Lets Improv: Theater Workshop</div>
            <div class="">
              Workshop using theatre techniques focussing on aspects, Embracing Failures, taking calculated risks, Working through constraints, and Building on ideas.
            </div>
          </div>
          <button onclick="popup('women-startup-summit-40-workshop-323431');" class="p-1 inline-block mx-auto bg-white text-red-700 shadow-md mt-5">
            <div class="border-4 border-red-600 shadow-md px-8 py-2">
              Register Now
            </div>
          </button>
        </div>
      </div>

      <div class="bg-red-600 text-white p-2">
        <div class="border-4 border-white h-full shadow-md p-4 text-center flex flex-col justify-between">
          <div>
            <div class="font-bold text-xl mb-3">Investor Cafe</div>
            <div class="">
              Investor café is an opportunity for startups looking for funds to connect with angel investors and VCs.
            </div>
          </div>
          <a href="https://forms.zohopublic.com/keralastartupmission/form/Startups/formperma/mED0NailX3wcajtbX4Yz_OY4PTW6LKlwAccKZVpsCt8" target="_blank"  class="p-1 inline-block mx-auto bg-white text-red-700 shadow-md mt-5">
            <div class="border-4 border-red-600 shadow-md px-8 py-2">
              Register Now
            </div>
          </a>
        </div>
      </div>

      <div class="bg-red-600 text-white p-2">
        <div class="border-4 border-white h-full shadow-md p-4 text-center flex flex-col justify-between">
          <div>
            <div class="font-bold text-xl mb-3">Women Founders Meet</div>
            <div class="">
              Exclusive Women Founders meet is planned at Kochi on september 23,2022. It is an invite-only event and entry is limited to malayali women founders. 
            </div>
          </div>
          <button onclick="popup('woman-founders-meet-213134');"  class="p-1 inline-block mx-auto bg-white text-red-700 shadow-md mt-5">
            <div class="border-4 border-red-600 shadow-md px-8 py-2">
              Register Now
            </div>
          </button>
        </div>
      </div>

      <div class="bg-red-600 text-white p-2">
        <div class="border-4 border-white h-full shadow-md p-4 text-center flex flex-col justify-between">
          <div>
            <div class="font-bold text-xl mb-3">Product Showcase</div>
            <!-- <div class="">
              Investor café is an opportunity for startups looking for funds to connect with angel investors and VCs.
            </div> -->
          </div>
          <a href="https://zfrmz.com/E00jM0lHIaKikIYTCuPy" target="_blank"  class="p-1 inline-block mx-auto bg-white text-red-700 shadow-md mt-5">
            <div class="border-4 border-red-600 shadow-md px-8 py-2">
              Register Now
            </div>
          </a>
        </div>
      </div>

    </div>

  </div>
  
</section>

<section class="py-20 px-5 bg-[#1a1a1a] text-white">

  <div class="container mx-auto flex md:flex-row flex-col justify-evenly items-center">
    <Info number="2" title="Days"></Info>
    <Info number="20+" title="Live Sessions"></Info>
    <Info number="30+" title="Speakers"></Info>
    <Info number="50+" title="Product Display"></Info>
    <Info number="500+" title="Attendees"></Info>
  </div>

</section>

<section id="programs" class="py-5 px-5 bg-[#1a1a1a] overflow-x-hidden">
  <div class="container mx-auto ">
    <div class="font-other font-bold text-4xl text-center mb-10 text-white">Tracks</div>
    <Tracks></Tracks>
  </div>
  <!-- <div class="">
    <div class="font-other font-bold text-4xl text-center mb-10 text-white">Workshops</div>

    <div class="grid gap-5 md:grid-cols-4">

      <button class="" onclick="popup('women-startup-summit-40-workshop-323431');">
        <img src="/wss/img/dt-w.png" alt="">
      </button>
      <button class="" onclick="popup('women-startup-summit-40-workshop-323431');">
        <img src="/wss/img/fab-w.png" alt="">
      </button>
      <button class="" onclick="popup('women-startup-summit-40-workshop-323431');">
        <img src="/wss/img/desgin-w.png" alt="">
      </button>

    </div>
  </div> -->
</section>

<!-- <section class="py-20 px-5 bg-[#1a1a1a] text-white">
  <div class="container mx-auto">
    <div class="grid md:grid-cols-3 gap-20">
      <div class="">
        <a href="/shelovestech">
          <img src="/wss/img/slt-poster.jpeg" alt="" >
        </a>
      </div>
      <div class="">
        <a href="https://grants.startupmission.in" target="_blank">
          <img src="/wss/img/grant-poster.jpeg" alt="" >
        </a>
      </div>
      <div class="">
        <a href="https://zfrmz.com/pXHr5Qgjqb19pc9k7SH9" target="_blank">
          <img src="/wss/img/herstart.jpeg" alt="" >
        </a>
      </div>
    </div>
  </div>
</section> -->

<section id="speakers" class="pt-20 pb-10 px-5 bg-[#1a1a1a] text-white">
  <div class="container mx-auto max-w-5xl">
    <div class="font-other font-bold text-4xl text-center mb-10">Our Speakers</div>

    <Speakers/>
  </div>
</section>

<section id="agenda" class="pt-10 pb-20 px-5 bg-[#1a1a1a] text-white">
  <div class="mx-auto container">
    <div class="font-other font-bold text-4xl text-center mb-10">Agenda</div>

    <Agenda/>
  </div>
</section>

<section id="partners" class="py-16 px-5 bg-[#f6f6f6]">
  <div class="container mx-auto">
    <div class="font-other font-bold text-4xl text-center mb-10">Our Partners</div>

    <div class="grid md:grid-cols-2 mb-10">
      <div class="">
        <div class="font-other font-bold text-xl text-center mb-2">National Partner</div>
        <Partners partners={national_partners} />
      </div>
      <div class="">
        <div class="font-other font-bold text-xl text-center mb-2">Media Partner</div>

        <Partners partners={media_partners}/>
      </div>
    </div>

    <div>
      <div class="font-other font-bold text-xl text-center mb-2">Ecosystem Partners</div>

      <Partners partners={eco_partners}/>
    </div>
  </div>
</section>


<section class="py-24 bg-[#1a1a1a] text-white">
  <div class="container mx-auto">
    <div class="flex flex-wrap">
      <div class="w-full md:w-1/2 bg-white border-8 border-white shadow">
        <iframe title="map" src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d15714.13294256542!2d76.3542335!3d10.0553212!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0xeaddd199d9bbde2b!2sKerala%20Technology%20Innovation%20Zone%20(KTIZ)!5e0!3m2!1sen!2sin!4v1655224297726!5m2!1sen!2sin" width="100%" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
      </div>
      <div class="w-full md:w-1/2 py-5 flex flex-col items-center justify-center">

        <img src="/wss/img/logo-white.svg" alt="LOGO" class="mb-3">

        <!-- <div class=" mb-2">
          Event Venue:
        </div> -->
        <div class="font-bold font-heading">Kerala Technology Innovation Zone</div>
        <div class="text-sm max-w-sm text-center">
          Kinfra Hi-Tech Park, Kalamassery, Kochi, Kerala, India
        </div>

        
        <div class="mt-10">
          For More Details:
        </div>
        <div class="font-bold font-heading">Sumi</div>
        <div class="">sumi@startupmission.in</div>
        <!-- <div class="">+91 95673 70286</div> -->

        <!-- <div class="text-center text-sm max-w-sm">G3B, Thejaswini, Technopark Campus, Kariyavattom, Trivandrum, Kerala 695581</div> -->
        
      </div>
    </div>
  </div>
</section>

<style lang="scss">
  .main-section{
    min-height: calc(100vh - 9.5rem);
  }
</style>
