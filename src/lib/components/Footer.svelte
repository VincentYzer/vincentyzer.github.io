<script lang="ts">
    export let tabs = [
        { name: "Facebook", link: "https://www.facebook.com/vincent.yzer", icon: "/assets/facebook.png" },
        { name: "Instagram", link: "https://www.instagram.com/rezy_vinx/", icon: "/assets/instagram.png" },
        { name: "GitHub", link: "https://github.com/VincentYzer", icon: "/assets/github.png" }
    ];
</script>

<header
    class="sticky z-[10] top-0 duration-200 px-6 flex items-center justify-between border-b border-solid py-3 bg-navy-900/95 backdrop-blur-sm border-purple-800/30"
>
    <h1 class="font-medium text-purple-100">
        <b class="font-bold poppins bg-gradient-to-r from-purple-200 to-cyan-200 bg-clip-text text-transparent">Yzer Vincent</b> 
        <span class="font-bold text-gray-200">De Omania</span>
    </h1>
    
    <div class="sm:flex items-center gap-6 hidden">
        {#each tabs as tab, index}
            <a
                href={tab.link}
                class="duration-200 text-gray-300 hover:text-purple-300 flex items-center gap-2 transition-all"
                target="_blank"
            >
                <div class="w-6 h-6 rounded-full bg-navy-800/80 p-1 backdrop-blur-sm border border-purple-700/20 transition-all hover:border-purple-500/30">
                    <img src={tab.icon} alt={`${tab.name} icon`} class="w-full h-full" />
                </div>
                <p class="text-sm">{tab.name}</p>
            </a>
        {/each}
        
        <button
            class="relative overflow-hidden px-6 py-2 group rounded-full bg-gradient-to-r from-purple-600 to-cyan-600 text-white transition-all duration-300 hover:shadow-lg hover:shadow-purple-500/20"
        >
            <div
                class="absolute top-0 right-full w-full h-full bg-gradient-to-r from-purple-400 to-cyan-400 opacity-20 group-hover:translate-x-full z-0 duration-300"
            />
            <a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ" class="relative z-9 text-sm font-medium" target="_blank">
                Click Me :P
            </a>
        </button>
    </div>
</header>