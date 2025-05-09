<script>
	// import Counter from '../lib/components/Counter.svelte';
	// import welcome from '$lib/images/svelte-welcome.webp';
	// import welcomeFallback from '$lib/images/svelte-welcome.png';
	import HeroSection from '$lib/components/HeroSection.svelte';
	import FeaturedProjects from '$lib/components/FeaturedProjects.svelte';
	import AboutPreview from '$lib/components/AboutPreview.svelte';
	import ContactCTA from '$lib/components/ContactCTA.svelte';
	import SiteFooter from '$lib/components/SiteFooter.svelte';
</script>

<svelte:head>
	<title>Rick Miskin | Software Engineer</title>
	<meta name="description" content="Full-stack software engineer building websites for local businesses and employers. View my work and résumé." />
</svelte:head>

<main class="px-4 sm:px-6 lg:px-8 py-12 space-y-24">
	<HeroSection />
	<FeaturedProjects />
	<AboutPreview />
	<ContactCTA />
</main>