<script lang="ts">
    import Header from '$lib/components/Header.svelte';
    import Footer from '$lib/components/Footer.svelte';

    const projects = [
        {
            title: "Project One",
            image: "/assets/Trafficlights.png",
            description: "This is the first coding that i did in which all of the teachings that our professor taught us. it uses a html, css and Javasript for the color switching of the colors.",
            technologies: ["Html", "CSS", "Javascript"]
        },
        {
            title: "Project Two",
            image: "/assets/Library.png",
            description: "This project is the Finals requirement in the subject Computer Programming in which the main IDE is Netbeans. It comprises of Java and MySql as the Database for the project",
            technologies: ["Java", "MySql", "JavaScript"]
        },
        {
            title: "Project Three",
            image: "/assets/Weatherapp.png",
            description: "This is the Finals project that I did in the Application Development subject. It uses an Angular Framework and it fetches a public Weather API in which the API key is hidden in the PHP file.",
            technologies: ["Angular", "Php", "Javascript","CSS"]
        }
    ];
</script>

<Header/>

<div class="min-h-screen bg-gradient-to-br from-navy-900 to-purple-900 text-gray-50 py-16 px-4 sm:px-6 lg:px-8">
    <div class="max-w-7xl mx-auto">
        <!-- Header -->
        <div class="text-center mb-16">
            <h1 class="text-5xl font-bold text-purple-200 mb-6">My Projects</h1>
            <p class="text-xl text-gray-300 max-w-3xl mx-auto">A showcase of my recent work and achievements in web development and design</p>
        </div>

     
        <div class="grid grid-cols-1 gap-16">
            {#each projects as project}
                <div class="group bg-navy-800/40 backdrop-blur-sm rounded-2xl overflow-hidden border border-navy-700/30 shadow-xl transition-all duration-300 hover:transform hover:scale-[1.01]">
                  
                    <div class="relative h-[400px] lg:h-[500px] overflow-hidden">
                        <img 
                            src={project.image} 
                            alt={project.title}
                            class="w-full h-full object-cover transition-transform duration-300 group-hover:scale-105"
                        />
                       
                        <div class="absolute inset-0 bg-gradient-to-t from-navy-900/80 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
                    </div>

              
                    <div class="p-8 lg:p-10 bg-gradient-to-b from-navy-800/60 to-purple-900/60">
                        <h3 class="text-2xl lg:text-3xl font-semibold text-purple-200 mb-4">{project.title}</h3>
                        
                    
                        <div class="flex flex-wrap gap-2 mb-6">
                            {#each project.technologies as tech}
                                <span class="px-4 py-1.5 text-sm bg-purple-800/50 text-purple-200 rounded-full border border-purple-700/30">
                                    {tech}
                                </span>
                            {/each}
                        </div>

                        
                        <p class="text-lg text-gray-200 leading-relaxed">
                            {project.description}
                        </p>
                    </div>
                </div>
            {/each}
        </div>
    </div>
</div>

<Footer/>