<script lang="ts">
    import Header from '$lib/components/Header.svelte';
    import Footer from '$lib/components/Footer.svelte';

    const education = {
        college: {
            school: "Gordon College",
            years: "2020 - Present",
            course: "Bachelor of Science in Information Technology",
            achievements: [
                "Dean's Lister 1st Semester AY 2022-2023",
                "Dean's Lister 2nd Semester AY 2022-2023",
                "Dean's Lister 1st Semester AY 2023-2024",
                "College of Computer Studies Student council officer",
            ]
        },
        seniorHigh: {
            school: "Regional Science High School III Senior High Department",
            years: "2018 - 2020",
            track: "Science, Technology, Engineering and Mathematics (STEM)",
            achievements: [
                "With High Honors",
                "Outstanding Capstone and Research",
                "Red Cross Youth Officer",
                "Perfect Attendance",
            ]
        },
        highSchool: {
            school: "Regional Science High School III",
            years: "2014 - 2018",
            achievements: [
                "With Honors",
                "Perfect Attendance",
                "Science Fair 1st placer"
            ]
        }
    };
</script>

<Header/>


<div class="h-[calc(100vh-8rem)] bg-viridian-900/50 text-gray-50 py-4 px-4 sm:px-6 lg:px-8 overflow-auto relative z-10">
    <div class="h-full max-w-6xl mx-auto grid grid-cols-12 gap-4">

        <!-- Personal Information Section -->
        <div class="col-span-12 lg:col-span-4">
            <div class="h-full bg-gradient-to-br from-navy-800/30 to-navy-900/40 backdrop-blur-sm rounded-2xl p-6 border border-navy-700/30 shadow-xl transition-all duration-300 hover:bg-navy-800/50">
                <div class="flex flex-col items-center text-center">
                    <div class="mb-6 rounded-full border-2 border-purple-400/50 shadow-xl overflow-hidden w-48 h-48">
                        <img 
                           src={"/assets/about-me.jpg"} 
                            alt="Yzer Vincent De Omania" 
                            class="w-full h-full object-cover"
                        />
                    </div>
                    <h1 class="text-3xl font-bold text-purple-200 mb-4">About Me</h1>
                    <div class="space-y-4">
                        <p class="text-lg text-gray-200">Hello! I'm <span class="text-purple-300 font-semibold">Yzer Vincent De Omania</span></p>
                        <p class="text-gray-200">As a 21-year-old aspiring developer born on August 12, 2003, I'm on an exciting journey through the world of 
                        Information Technology. Currently based in the vibrant city of Olongapo, 
                        I'm pursuing my passion for web development and a Network Administrator.</p>
                        <p class="text-gray-200">My goal is to become a Network Administrator, I'm particularly interested in the world of Networking, 
                        and I'm excited to see how it will affect and shape our digital future.</p>
                        <ul class="text-gray-200 text-left">
                            <li><span class="text-purple-300 font-semibold">Age:</span> 21</li>
                            <li><span class="text-purple-300 font-semibold">Birthday:</span> August 12, 2003</li>
                            <li><span class="text-purple-300 font-semibold">Location:</span> Olongapo City</li>
                            <li><span class="text-purple-300 font-semibold">Education:</span> BSIT Student</li>
                            <li><span class="text-purple-300 font-semibold">Interests:</span> Web Development, Network Administrator</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>

        <!-- Educational Background -->
        <div class="col-span-12 lg:col-span-8 grid grid-rows-3 gap-4">
            <!-- College -->
            <div class="bg-gradient-to-r from-navy-800/30 to-navy-900/40 backdrop-blur-sm rounded-2xl p-4 border border-navy-700/30 shadow-xl hover:scale-[1.01] hover:bg-navy-800/50 transition-all duration-300">
                <div class="flex justify-between items-start">
                    <div>
                        <h2 class="text-xl font-bold text-cyan-200">{education.college.school}</h2>
                        <p class="text-gray-300 text-sm">{education.college.years}</p>
                        <p class="text-cyan-300 text-sm">{education.college.course}</p>
                    </div>
                    <div class="text-right">
                        <h3 class="text-lg font-semibold text-cyan-200 mb-1">Achievements</h3>
                        <ul class="text-gray-100 text-lg space-y-0.5">
                            {#each education.college.achievements as achievement}
                                <li>{achievement}</li>
                            {/each}
                        </ul>
                    </div>
                </div>
            </div>
            <!-- Senior High School -->
            <div class="bg-gradient-to-r from-navy-800/30 to-purple-900/40 backdrop-blur-sm rounded-2xl p-4 border border-navy-700/30 shadow-xl hover:scale-[1.01] hover:bg-navy-800/50 transition-all duration-300">
                <div class="flex justify-between items-start">
                    <div>
                        <h2 class="text-xl font-bold text-purple-200">{education.seniorHigh.school}</h2>
                        <p class="text-gray-300 text-sm">{education.seniorHigh.years}</p>
                        <p class="text-purple-300 text-sm">{education.seniorHigh.track}</p>
                    </div>
                    <div class="text-right">
                        <h3 class="text-lg font-semibold text-purple-200 mb-1">Achievements</h3>
                        <ul class="text-gray-100 text-lg space-y-0.5">
                            {#each education.seniorHigh.achievements as achievement}
                                <li>{achievement}</li>
                            {/each}
                        </ul>
                    </div>
                </div>
            </div>

            <!-- High School -->
            <div class="bg-gradient-to-r from-navy-800/30 to-blue-900/40 backdrop-blur-sm rounded-2xl p-4 border border-navy-700/30 shadow-xl hover:scale-[1.01] hover:bg-navy-800/50 transition-all duration-300">
                <div class="flex justify-between items-start">
                    <div>
                        <h2 class="text-xl font-bold text-blue-200">{education.highSchool.school}</h2>
                        <p class="text-gray-100 text-sm">{education.highSchool.years}</p>
                    </div>
                    <div class="text-right">
                        <h3 class="text-lg font-semibold text-blue-200 mb-1">Achievements</h3>
                        <ul class="text-gray-100 text-lg space-y-0.5">
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