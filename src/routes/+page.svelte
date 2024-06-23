  
  <script>

    import SR from "$lib/icons/squerRoot.svelte";
    import MS from "$lib/icons/minus.svelte";
    import D from "$lib/icons/div.svelte";
    import MN from "$lib/icons/multiplication.svelte";
    import PL from "$lib/icons/plus.svelte";
    import EQ from "$lib/icons/equal.svelte";
  </script>
  <svelte:head>
    <title>
      calculator
    </title>
  </svelte:head> 
  <div class="bg-white  rounded-3xl grid grid-cols-4 gap-1 p-4 font-semibold text-xl shadow-2xl">
  <div class="bg-[#3978ff] rounded-full flex justify-start items-start text-white col-span-4 h-12 flex items-center px-4 mb-2">
12345  
  </div>
<button class="bg-[#f3f6fc]">%</button>
<button class="bg-[#f3f6fc] " > <SR/></button>
<button class="bg-[#f3f6fc]">CE</button>
<button class="bg-[#1f2b54] text-white">C</button>
<button  >7</button>
<button >8</button>
<button>9</button>
<button class="bg-[#fd3f59] text-white"><MS/></button>
<button>4</button>
<button>5</button>
<button>6</button>
<button class="bg-[#2285fd] text-white "><D/></button>
<button>1</button>
<button>2</button>
<button>3</button>
<button class="bg-[#f9c80e] text-white "><MN/></button>
<button>.</button>
<button>0</button>
<button  class="bg-[#f3f6fc]"><EQ/> </button>
<button class="bg-[#63dc74] text-white" ><PL/></button>
</div>