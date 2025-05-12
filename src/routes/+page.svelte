<script>
	import HeroSection from '$lib/components/HeroSection.svelte';
	import FeaturedProjects from '$lib/components/FeaturedProjects.svelte';
	import AboutPreview from '$lib/components/AboutPreview.svelte';
	import ContactCTA from '$lib/components/ContactCTA.svelte';
</script>

<svelte:head>
	<title>Rick Miskin | Software Engineer</title>
	<meta name="description" content="Full-stack software engineer building websites for local businesses and employers. View my work and résumé." />
</svelte:head>

<div class="bg-white">
	<HeroSection />
</div>
<div class="bg-gray-100">
	<FeaturedProjects />
</div>
<div class="bg-white">
	<AboutPreview />
</div>
<div class="bg-gray-100">
	<ContactCTA />
</div>