<script lang=ts>
    import Header from '$lib/components/Header.svelte';
    import Footer from '$lib/components/Footer.svelte';
    import { assets } from "$app/paths";
</script>

<div class="flex flex-col min-h-screen">
    <Header/>

    <main class="flex-grow flex items-center justify-center p-4 md:p-8 overscroll-none">
        <section id="landingPage" class="w-full max-w-7xl mx-auto grid grid-cols-1 lg:grid-cols-2 gap-8 lg:gap-12">
            <div class="flex flex-col justify-center text-center lg:text-left gap-6 lg:gap-8">
                <h2 class="font-semibold text-4xl sm:text-5xl lg:text-6xl">
                    Hi I'm <span class="poppins text-violet-600">Yzer Vincent</span> 
                    <span class="text-bold">De Omania</span> <br/>
                    A College <span class="poppins text-violet-600">Student</span> 
                </h2>
                <p class="text-base sm:text-lg lg:text-xl">
                    <span class="text-violet-500">WELCOME</span> to my website. I am a 3rd year BSIT student currently studying at
                    Gordon College, Olongapo City. I am a back-end developer with knowledge of Java, MySQL, Php, Html and Css and Javascript.
                    I am always eager to learn and grow as a developer. Feel free to reach out if you need help with any projects or if you are interested in learning more about me. 
                    Feel free to explore my website.
                </p>
            </div>
            <div class="flex justify-center items-center">
                <img 
                    src={"/assets/Profile-pic.jpg"} 
                    alt="Yzer Vincent De Omania" 
                    class="w-64 h-64 sm:w-80 sm:h-80 lg:w-96 lg:h-96 rounded-full object-cover"
                />
            </div>
        </section>
    </main>

    <Footer/>
</div>