<script>

  let menu_open;

  let y = 0;

  $: scrolled = y > 200;

  function findPos(obj) {
    var curtop = 0;
    if (obj.offsetParent) {
        do {
            curtop += obj.offsetTop;
        } while (obj = obj.offsetParent);
    return [curtop];
    }
  }

  const handleCyclo = (e) => {
    e.preventDefault()
    let button = e.target.closest('[data-target]');
    let target = button.getAttribute('data-target');
    let offset = button.getAttribute('data-offset');
    
    window.scroll({
      left:0,
      top:findPos(document.getElementById(target))-offset, 
      behavior:'smooth'
    });

    menu_open = !menu_open
    
  }

</script>

<svelte:window bind:scrollY={y}/>

<div id="navbar" class=" w-64 min-h-screen sm:w-full sm:min-h-0 sm:h-20 bg-[#1a1a1a]  left-0 top-0 
    sm:flex ease-in-out transition-all transform duration-300
    -translate-x-full sm:translate-x-0 fixed md:sticky z-10 
     {menu_open?'translate-x-0':''} 
    ">
  
    <div class="w-full container mx-auto sm:flex sm:items-end sm:justify-between">
      <div class="flex justify-center items-center {scrolled ? '' : 'md:hidden'} pb-2">
        <!-- <img src="/img/slt-logo.png" alt="" class="h-16"> -->
        <img src="/img/logo-white.svg"  alt="" class="h-14">
      </div>

      <nav class="justify-center items-center text-center mx-auto">
        <ul class="sm:flex md:text-sm ">

          <!-- <li class="px-5 md:pb-5 border-b-4 border-transparent hover:border-red-600">
            <a on:click={handleCyclo} data-target="speakers" data-offset="70" href="/" class="font-other text-white px-2 py-1 font-bold">Previous Speakers</a>
          </li> -->

          <li on:click={handleCyclo} data-target="partners" data-offset="70" class="px-5 md:pb-5 border-b-4 border-transparent hover:border-red-600">
            <a href="/" class="font-other text-white px-2 py-1 font-bold">Our Partners</a>
          </li>

          <li class="px-5 md:pb-5 border-b-4 border-transparent hover:border-red-600">
            <a on:click={handleCyclo} data-target="agenda" data-offset="70" href="/" class="font-other text-white px-2 py-1 font-bold">Agenda</a>
          </li>

          <li class="px-5 md:pb-5 border-b-4 border-transparent hover:border-red-600">
            <a target="_blank" href="https://forms.zohopublic.com/keralastartupmission/form/WOMENSTARTUPSUMMIT5O2023/formperma/BpxTdb5GjId36n61eFW5ZBSFsLCbFae_xUSriLEDbpo" class="font-other text-white px-2 py-1 font-bold">Sign Up for Updates</a>
          </li>
        </ul>
        
      </nav>

      <div class="md:pb-3">
        <a target="_blank" href="/shelovestech" class="inline-block font-other text-white px-4 md:px-8 py-3 bg-red-600 hover:bg-red-500">She Loves Tech India</a>
      </div>
    </div>

</div>

<!-- <main class="w-full">
  <div class="flex sm:hidden p-3 bg-white shadow">        
    <img src="{base}/img/logo.svg" alt="Logo" class="object-contain h-12">
    
  </div>
</main> -->
