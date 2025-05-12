<script>
  import ProjectCard from '$lib/components/ProjectCard.svelte';
  import svelteLogo from '$lib/images/sveltekit-img1.jpg';
  import hhcLogo from '$lib/images/hhc-logo.jpg';
  import dadjokeLogo from '$lib/images/dad-joke-logo.jpg';
  import missingImage from '$lib/images/missing-image.jpg';

  const projects = [
    {
      title: "Dad Joke Generator",
      description: "Demo API calls SvelteKit and Tailwind. It's fun!",
      image: dadjokeLogo,
      url: "https://www.rickmiskin.dev/dad-joke"
    },
    {
      title: "Sverdle",
      description: "Wordle but written using Svelte!",
      image: svelteLogo,
      url: "https://www.rickmiskin.dev/sverdle"
    },
    {
      title: "Hunt Hook & Cook",
      description: "A website I built for a friend's business using MudBlazor.",
      image: hhcLogo,
      url: "https://hunthookandcook-dgdjb6dwhqcghyh8.eastus2-01.azurewebsites.net"
    },
    {
      title: "Missing Image",
      description: "A placeholder image for projects without a logo.",
      image: missingImage,
      url: "#"
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
