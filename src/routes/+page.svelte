<main class="h-screen flex justify-center">
    <section class="w-7/12 pt-30 pl-5 border">
        <div class="grid grid-cols-[100px_1fr] grid-rows-2">
            <!-- First row -->
            <div class="text-7xl col-start-1 col-end-2 row-span-full ">{currentEmoji}</div>
            <h1 class="font-display text-5xl text-gray-700 pt-1 pl-2">Elijah Mejilla</h1>
        
            <h3 class="font-display text-lg pt-0.5 pl-2 text-gray-400 italic">web developer, writer</h3>
        </div>  
    </section>
</main> 

<script lang="ts">
    import { onMount, onDestroy } from "svelte";

    let intervalId;
    const interval = 2.5
    const emojis = $state(['🌱', '🖋️', '🎻', '✏️'])
    let currentEmoji = $derived(emojis[0])

    function changeEmoji() {
        let popped: string = emojis.shift()
        emojis.push(popped) 
    }
    onMount(() => {
        intervalId = setInterval(changeEmoji, interval * 1000)

        return() => {
            clearInterval(intervalId)
        }
    })

    onDestroy(() => {
        if (intervalId) {
            clearInterval(intervalId)
        }
    })
</script>