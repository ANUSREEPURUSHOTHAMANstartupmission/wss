<script>
  export let number;
  export let title;
</script>
<div class="relative w-40 h-40  mb-5 text-center text-white  ">
  

  <div class="absolute transform rotate-[22deg] rounded-full rounded-tr-none shadow-lg w-full h-full bg-red-600 hover:bg-red-500 border-t-2 border-r-2"></div>
  <div class="absolute transform rotate-[67deg] rounded-full rounded-tr-none shadow-lg w-full h-full bg-red-600 hover:bg-red-500 border-t-2 border-r-2"></div>
  <div class="absolute transform rotate-[0deg] rounded-full rounded-tr-none shadow-lg w-full h-full bg-red-600 hover:bg-red-500 border-t-2 border-r-2"></div>
  <div class="absolute transform rotate-[-22deg] rounded-full rounded-tr-none shadow-lg w-full h-full bg-red-600 hover:bg-red-500 border-t-2 border-r-2"></div>
  <div class="absolute transform rotate-[-67deg] rounded-full rounded-tr-none shadow-lg w-full h-full bg-red-600 hover:bg-red-500 border-t-2 border-r-2"></div>

  <div class="absolute transform rotate-45 rounded-full rounded-tl-lg rounded-tr-none shadow-lg w-full h-full bg-red-600 hover:bg-red-500 border-t-2 border-r-2 border-l-2"></div>

  <div class="flex flex-col items-center justify-center h-full w-full absolute">
    <div class="text-5xl font-black mb-3">{number}</div>
    <div class="">{title}</div>
  </div>
</div>