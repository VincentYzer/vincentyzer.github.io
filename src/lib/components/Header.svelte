<script>
    export let tabs = [
        { name: "Projects ", link: "/projects" },
        { name: "About me", link: "/about me" },
    ];
</script>

<header
    class="sticky z-[10] top-0 duration-200 px-6 flex items-center justify-between border-b border-solid py-4 bg-navy-900 border-navy-800"
>
    <h1 class="font-medium">
        <a href="/" class="duration-200 hover:text-purple-400">
            <b class="font-bold poppins text-4xl">VYD</b>
        </a>
    </h1>
    <div class="sm:flex items-center gap-4 hidden">
        {#each tabs as tab, index}
            <a
                href={tab.link}
                class="duration-200 hover:text-purple-400"
                target={index === 3 ? "_blank" : ""}
            >
                <p>{tab.name}</p>
            </a>
        {/each}
    </div>
</header>