<script lang="ts">
      import "../app.css";
      import Footer from "$lib/components/Footer.svelte";
      import Header from "$lib/components/Header.svelte";
    
      let y: number = 0;
      let innerHeight = 0;
      let innerWidth = 0;
    
      function goToTop(){
        document.body.scrollIntoView()
      }
    </script>
    
    
    <svelte:head>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin="anonymous">
    <link href="https://fonts.googleapis.com/css2?family=Fredoka:wght@300..700&display=swap" rel="stylesheet">
    </svelte:head>
    
    <div class ="relative flex flex-col max-w-[1400px] mx-auto w-full text-sm sm:text-base min-h-screen">
        <div class="fixed bottom-0 w-full duration-200 flex p-10 z-[10] ">
            <button on:click={goToTop} class="ml-auto rounded-full bg-slate-600 text-purple-400 px- sm:px-4 hover: bg-slate-500 cursor-pointer">
                <i class="fa-solid fa-arrow-up grid place-items-center aspect-square"/>
            </button>
        </div>
  
        <slot/>
       <!--<Footer/> -->
    </div>
    
    <svelte:window bind:scrollY={y} bind:innerHeight bind:innerWidth/>