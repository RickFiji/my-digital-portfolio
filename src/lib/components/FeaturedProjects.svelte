<script>
  import ProjectCard from '$lib/components/ProjectCard.svelte';
  import dadjokeLogo from '$lib/images/dad-joke-logo.jpg';
  import pathToSalvationLogo from '$lib/images/path-to-salvation-logo.png';

  const featuredProjects = [
    {
      title: "Path to Salvation",
      description: "A minimal, step-by-step micro-app presenting the biblical path to salvation through KJV Scripture.",
      image: pathToSalvationLogo,
      url: "https://path-to-salvation.lovable.app"
    },
    {
      title: "Dad Joke Generator",
      description: "Demo API calls SvelteKit and Tailwind. It's fun!",
      image: dadjokeLogo,
      url: "/dad-joke"
    }
  ];
</script>

<section class="text-center bg-gray-50 py-10 px-6 rounded-lg shadow-sm">
  <h2 class="text-xl font-semibold mb-6">Featured Projects</h2>
  <div class="grid gap-6 sm:grid-cols-2 ml-6 mr-6">
      {#each featuredProjects as project}
          <ProjectCard 
              title={project.title}
              description={project.description}
              image={project.image}
              url={project.url}
          />
      {/each}
  </div>
</section>