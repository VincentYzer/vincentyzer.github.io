<script lang=ts>
    import Header from '$lib/components/Header.svelte';
    import Footer from '$lib/components/Footer.svelte';
    import { assets } from "$app/paths";
</script>

<Header/>

  <main class="flex flex-col flex-1 p-4">
      <secton id ="landingPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
          <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
              <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl"> Hi I'm <span class="poppins text-violet-600">
                  Yzer Vincent</span> <span class="text-bold">De Omania</span> <br/>A College <span class="poppins text-violet-600">Student</span> 
              </h2>
              <p class="text-base sm:text-lg md:text-xl">
                  My <span class="text-violet-500"> Favorite Tech</span> includes Javascript (Next.JS or SvelteKit), Tailwindcss.
                  Node.js + Express.js & postgreSQL or Firebase/Firestore!
              </p>
          </div>
          <div class="relative shadow-2xl grid place-items-center">
            <img 
            src={"/assets/Profile-pic.jpg"} 
            alt= "Yzer Vincent De Omania" 
            class="object-cover z-[2] max-h-[70]"
        />
          </div>
      </secton>
  </main>

<!--<Footer/>-->