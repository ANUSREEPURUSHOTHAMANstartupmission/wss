<script>
  let open = false;

  export let items = [];
  export let title = '';
</script>

<div class="relative inline-block text-left z-10">

  <div on:click={()=>{open = !open}}>
    <button type="button" class="inline-flex justify-center w-full text-white hover:bg-slate-900  px-5 py-3 text-sm font-medium " id="menu-button" aria-expanded="true" aria-haspopup="true">
      {title}
      <!-- Heroicon name: solid/chevron-down -->
      <svg class="-mr-1 ml-2 h-5 w-5 trasnition duration-300 transform {open ? 'rotate-180' : ''}" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
        <path fill-rule="evenodd" d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" clip-rule="evenodd" />
      </svg>
    </button>
  </div>

  {#if open}
    <div class="origin-top-right absolute right-0 mt-2 w-56 bg-black text-white" role="menu" aria-orientation="vertical" aria-labelledby="menu-button" tabindex="-1">
      <div class="py-1" role="none">
        <!-- Active: "bg-gray-100 text-gray-900", Not Active: "text-gray-700" -->
        {#each items as item}
          <a href="{item.link}" target="{item.target ?? ''}" class="block px-5 py-3 border-b border-slate-800 text-sm hover:bg-slate-900" role="menuitem" tabindex="-1" id="menu-item-0">{item.label}</a>
        {/each}
      </div>
    </div>
  {/if}

</div>