  
  <script lang="ts">

    import SR from "$lib/icons/squerRoot.svelte";
    import MS from "$lib/icons/minus.svelte";
    import D from "$lib/icons/div.svelte";
    import MN from "$lib/icons/multiplication.svelte";
    import PL from "$lib/icons/plus.svelte";
    import EQ from "$lib/icons/equal.svelte";
    function addtoEqution(value:string){
      equation+=value;
    };
    function remAll(){
      equation="";
    };
    function remlast(){
      const myspilt=equation.split(" ");
 myspilt.pop();
equation=myspilt.join(" ");
    };
    let equation:string="";
    let value:string;
    let lw:string;
    let sr:number;
    function sqR(){
      const sr=Math.sqrt(eval(equation));
      equation=sr.toString();
    }
    function eq(){
      equation=eval(equation);
    }
  </script>
  <svelte:head>
    <title>
      calculator
    </title>
  </svelte:head> 
  <div class="bg-white  rounded-3xl grid grid-cols-4 gap-1 p-4 font-semibold text-xl shadow-2xl max-w-[14.5rem] ">
  <div class="bg-[#3978ff] rounded-xl flex justify-start items-start text-white col-span-4 min-h-12 flex items-center px-4 mb-2 break-all ">
  {equation}
  </div>
<button on:click={()=>addtoEqution(" /100")} class="bg-[#f3f6fc]">%</button>
<button on:click={()=>sqR()} class="bg-[#f3f6fc]" > <SR/></button>
<button on:click={()=>remlast()} class="bg-[#f3f6fc]">CE</button>
<button on:click={()=>remAll()} class="bg-[#1f2b54] text-white">C</button>
<button on:click={()=>addtoEqution("7")}>7</button>
<button on:click={()=>addtoEqution("8")}>8</button>
<button on:click={()=>addtoEqution("9")}>9</button>
<button on:click={()=>addtoEqution(" - ")} class="bg-[#fd3f59] text-white"><MS/></button>
<button on:click={()=>addtoEqution("4")}>4</button>
<button on:click={()=>addtoEqution("5")}>5</button>
<button on:click={()=>addtoEqution("6")}>6</button>
<button on:click={()=>addtoEqution(" / ")} class="bg-[#2285fd] text-white "><D/></button>
<button on:click={()=>addtoEqution("1")} >1</button>
<button on:click={()=>addtoEqution("2")}>2</button>
<button on:click={()=>addtoEqution("3")}>3</button>
<button on:click={()=>addtoEqution(" * ")} class="bg-[#f9c80e] text-white "><MN/></button>
<button on:click={()=>addtoEqution(".")}>.</button>
<button on:click={()=>addtoEqution("0")}>0</button>
<button on:click={()=>eq()} class="bg-[#f3f6fc]"><EQ/> </button>
<button on:click={()=>addtoEqution(" + ")} class="bg-[#63dc74] text-white" ><PL/></button>
</div>