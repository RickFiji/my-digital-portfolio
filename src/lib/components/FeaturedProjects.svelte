<script>
  import ProjectCard from '$lib/components/ProjectCard.svelte';
  import svelteLogo from '$lib/images/sveltekit-img1.jpg';
  import dadjokeLogo from '$lib/images/dad-joke-logo.jpg';

  const featuredProjects = [
    {
      title: "Dad Joke Generator",
      description: "Demo API calls SvelteKit and Tailwind. It's fun!",
      image: dadjokeLogo,
      url: "/dad-joke"
    },
    {
      title: "Sverdle",
      description: "Wordle but written using Svelte!",
      image: svelteLogo,
      url: "/sverdle"
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