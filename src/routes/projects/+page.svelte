<script>
  import ProjectCard from '$lib/components/ProjectCard.svelte';
  import image from '$lib/images/svelte-logo.svg';

  const projects = [
    {
      title: "Project One",
      description: "A website I built for a local business using SvelteKit and Tailwind.",
      image: image,
      url: "https://google.com/"
    },
    {
      title: "Project Two",
      description: "A modern portfolio site built with accessibility and speed in mind.",
      image: image,
      url: "https://google.com/"
    },
    {
      title: "Project Three",
      description: "A full-stack web app with authentication and dashboard functionality.",
      image: image,
      url: "https://google.com/"
    }
  ];
</script>

<svelte:head>
  <title>Projects | Rick Miskin</title>
  <meta name="description" content="A full showcase of Rick Miskin's web development projects." />
</svelte:head>

<section class="py-12 space-y-8">
  <h1 class="text-3xl font-bold text-center">My Projects</h1>
  <p class="text-center text-gray-600 max-w-xl mx-auto">
    A selection of websites and applications I've built — from local business sites to modern full-stack apps.
  </p>

  <div class="grid gap-6 sm:grid-cols-2 lg:grid-cols-3">
    {#each projects as project}
      <ProjectCard 
        title={project.title}
        description={project.description}
        image={project.image}
        url={project.url}
      />
    {/each}
  </div>
</section>
