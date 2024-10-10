<script lang="ts">
    import Header from '$lib/components/Header.svelte';
    import Footer from '$lib/components/Footer.svelte';

    const education = {
        college: {
            school: "Your University Name",
            years: "2020 - Present",
            course: "Bachelor of Science in Information Technology",
            achievements: [
                "Dean's Lister",
                "Best in Programming",
                "Academic Excellence Award"
            ]
        },
        seniorHigh: {
            school: "Your Senior High School",
            years: "2018 - 2020",
            track: "STEM",
            achievements: [
                "With High Honors",
                "Best in Research",
                "Science Club President"
            ]
        },
        highSchool: {
            school: "Your High School",
            years: "2014 - 2018",
            achievements: [
                "First Honor",
                "Mathematics Quiz Bee Champion",
                "Student Council Officer"
            ]
        }
    };
</script>

<Header/>


<div class="h-[calc(100vh-8rem)] bg-viridian-900 text-gray-50 py-4 px-4 sm:px-6 lg:px-8 overflow-hidden">
    <div class="h-full max-w-6xl mx-auto grid grid-cols-12 gap-4">
        <!-- Personal Information Section -->
        <div class="col-span-12 lg:col-span-4">
            <div class="h-full bg-navy-800/40 backdrop-blur-lg rounded-2xl p-6 border border-navy-700/30 shadow-xl">
                <div class="flex flex-col items-center text-center">
                    <!-- Added image container with border and shadow -->
                    <div class="mb-6 rounded-full border-2 border-purple-400/50 shadow-xl overflow-hidden w-48 h-48">
                        <img 
                           src={"/assets/about-me.jpg"} 
                            alt= "Yzer Vincent De Omania" 
                            class="w-full h-full object-cover"
                        />
                    </div>
                    <h1 class="text-3xl font-bold text-purple-200 mb-4">About Me</h1>
                    <div class="space-y-4">
                        <p class="text-lg text-gray-200">Hello! I'm <span class="text-purple-300 font-semibold">Your Name</span></p>
                        <p class="text-gray-300">Currently pursuing my degree in Information Technology, 
                        I specialize in web development and software engineering.</p>
                    </div>
                </div>
            </div>
        </div>

        <!-- Educational Background -->
        <div class="col-span-12 lg:col-span-8 grid grid-rows-3 gap-4">
            <!-- College -->
            <div class="bg-navy-800/40 backdrop-blur-lg rounded-2xl p-4 border border-navy-700/30 shadow-xl hover:scale-[1.01] transition-transform duration-300">
                <div class="flex justify-between items-start">
                    <div>
                        <h2 class="text-xl font-bold text-cyan-200">{education.college.school}</h2>
                        <p class="text-gray-300 text-sm">{education.college.years}</p>
                        <p class="text-cyan-300 text-sm">{education.college.course}</p>
                    </div>
                    <div class="text-right">
                        <h3 class="text-sm font-semibold text-cyan-200 mb-1">Achievements</h3>
                        <ul class="text-gray-300 text-sm space-y-0.5">
                            {#each education.college.achievements as achievement}
                                <li>{achievement}</li>
                            {/each}
                        </ul>
                    </div>
                </div>
            </div>

            <!-- Senior High School -->
            <div class="bg-navy-800/40 backdrop-blur-lg rounded-2xl p-4 border border-navy-700/30 shadow-xl hover:scale-[1.01] transition-transform duration-300">
                <div class="flex justify-between items-start">
                    <div>
                        <h2 class="text-xl font-bold text-purple-200">{education.seniorHigh.school}</h2>
                        <p class="text-gray-300 text-sm">{education.seniorHigh.years}</p>
                        <p class="text-purple-300 text-sm">{education.seniorHigh.track}</p>
                    </div>
                    <div class="text-right">
                        <h3 class="text-sm font-semibold text-purple-200 mb-1">Achievements</h3>
                        <ul class="text-gray-300 text-sm space-y-0.5">
                            {#each education.seniorHigh.achievements as achievement}
                                <li>{achievement}</li>
                            {/each}
                        </ul>
                    </div>
                </div>
            </div>

            <!-- High School -->
            <div class="bg-navy-800/40 backdrop-blur-lg rounded-2xl p-4 border border-navy-700/30 shadow-xl hover:scale-[1.01] transition-transform duration-300">
                <div class="flex justify-between items-start">
                    <div>
                        <h2 class="text-xl font-bold text-blue-200">{education.highSchool.school}</h2>
                        <p class="text-gray-300 text-sm">{education.highSchool.years}</p>
                    </div>
                    <div class="text-right">
                        <h3 class="text-sm font-semibold text-blue-200 mb-1">Achievements</h3>
                        <ul class="text-gray-300 text-sm space-y-0.5">
                            {#each education.highSchool.achievements as achievement}
                                <li>{achievement}</li>
                            {/each}
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>

<Footer/>