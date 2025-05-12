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

<section>
  <h2 class="text-2xl font-semibold text-center mb-6">Featured Projects</h2>

  <div class="grid gap-6 sm:grid-cols-2">
      {#each featuredProjects as project}
          <ProjectCard 
              title={project.title}
              description={project.description}
              image={project.image}
              url={project.url}
          />
      {/each}
  </div>

  <div class="mt-6 text-center">
      <a href="/projects" class="text-blue-600 hover:underline">
          View all projects →
      </a>
  </div>
</section>