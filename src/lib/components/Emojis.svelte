<script lang="ts">
    import { onMount, onDestroy } from "svelte";

    const interval = 3
    const emojis = $state(['🌱', '💻', '✏️', '🎻', '♟️'])
    // const emojis = $state(['🌱'])

    let intervalId; 
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

<span class="text-black">{currentEmoji}</span>