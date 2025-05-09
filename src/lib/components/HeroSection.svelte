<script>
    import headshot from '$lib/images/headshot-doge.jpg';
	import welcome from '$lib/images/svelte-welcome.webp';
	import welcomeFallback from '$lib/images/svelte-welcome.png';
</script>
  
<section class="text-center py-16">
<picture>
    <source srcset={welcome} type="image/webp" />
    <img src={welcomeFallback} alt="Welcome" />
</picture>

<img 
    src={headshot} 
    alt="Rick Miskin headshot" 
    class="mx-auto rounded-full w-32 h-32 object-cover mb-6 border-4 border-blue-600"
/>

<h1 class="text-3xl sm:text-4xl font-bold">Hi, I'm Rick Miskin</h1>
<p class="mt-3 text-lg text-gray-600">
    Full-stack developer building modern, fast websites for employers and local businesses.
</p>

<div class="mt-6 space-x-4">
    <a 
    href="/resume" 
    class="bg-blue-600 text-white px-5 py-2 rounded-md hover:bg-blue-700 transition"
    aria-label="View Résumé"
    >
    View Résumé
    </a>
    <a 
    href="/contact" 
    class="border border-blue-600 text-blue-600 px-5 py-2 rounded-md hover:bg-blue-50 transition"
    >
    Contact Me
    </a>
</div>
</section>