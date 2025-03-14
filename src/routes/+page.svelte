<script>
    import background from '$lib/images/background (11).png'
    import Emojis from '$lib/components/Emojis.svelte'
    import Subsection from '$lib/components/Subsection.svelte' 
</script>

<main class="h-screen flex justify-center bg-no-repeat font-display"
style="background-image: url('{background}'); background-size: 100% auto;
background-position: center 1%">
    <section class="w-7/12 pt-24 mt-45">
        <div class="flex flex-col">
            <!-- First row -->
            <h1 class="text-6xl py-1.5
            text-dark-blue">Elijah Mejilla <Emojis /></h1>
            <h3 class="font-display text-xl text-gray-400 italic">web developer & writer</h3>
        </div>  

        <div class="font-display my-10 text-lg/8 text-gray-700 max-w-prose">
            <p class="mb-5">Hey there! I'm Elijah—an aspiring web developer and computer scientist.</p>
            <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</p>
        </div>
        <Subsection text="projects"/>

        <div class="h-screen"></div>
    </section>
</main> 

<div class="absolute left-16 top-200 text-gray-400 cursor-pointer">
    <pre class="font-display">
　　　　　 　 ____        
　　　　　／＞　　フ     
　　　　　| 　_　 _ l  
　 　　　／` ミ＿xノ
　　 　 /　　　 　 |   
　　　 /　 ヽ　　 ﾉ
　 　 │　　|　|　|
　／￣|　　 |　|　|
　| (￣ヽ＿ヽ)__) __)
　＼二つ
    </pre>
</div>

<div class="absolute right-25 top-320 text-gray-400 cursor-pointer">
    <pre class="font-display">
⠀ ／l、
（ﾟ､ ｡ ７
⠀ l、ﾞ ~ヽ
  じしf_, )ノ
</pre>
</div>