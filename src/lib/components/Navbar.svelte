<main class="fixed text-xl py-10 w-full h-18 flex items-center justify-center
backdrop-blur-lg font-mono font-bold">
    <nav class="flex w-7/12 h-full items-center justify-between gap-10 text-dark-blue">
        <div class="flex gap-10">
            {#each [
                {'text': 'home', 'path': '/'}, 
                {'text': 'cv', 'path': '/cv'}, 
                {'text': 'blog', 'path': '/blog'}
                ] as item}
                <a href="{item['path']}" class="hover:text-red-400 cursor-pointer">{item['text']}</a>
            {/each}
        </div>
        <div class="flex gap-10">
            {#each [
                {'text': 'github', 'url': 'https://github.com/jgmejilla/'}, 
                {'text': 'linkedin', 'url': 'https://www.linkedin.com/in/jgmejilla/'}, 
                ] as item}
            <a target="_blank" href="{item['url']}" class="hover:text-red-400 cursor-pointer">{item['text']}</a>
            {/each}
        </div>
        
    </nav>
</main>

