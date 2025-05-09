<script>
	import logo from '$lib/images/svelte-logo.svg';
  
  const featuredProjects = [
    {
      title: "Project One",
      description: "A short blurb about this project.",
      image: logo,
      url: "https://example.com/project1"
    },
    {
      title: "Project Two",
      description: "Another awesome project.",
      image: logo,
      url: "https://example.com/project2"
    }
  ];
</script>

<section>
    <h2 class="text-2xl font-semibold text-center mb-6">Featured Projects</h2>

    <div class="grid gap-6 sm:grid-cols-2">
        {#each featuredProjects as project}
        <a 
            href={project.url} 
            target="_blank" 
            rel="noopener noreferrer" 
            class="block border rounded overflow-hidden hover:shadow-lg transition bg-white"
        >
            <img 
            src={project.image} 
            alt={project.title} 
            class="w-full h-48 object-cover"
            />
            <div class="p-4">
            <h3 class="text-xl font-semibold">{project.title}</h3>
            <p class="text-gray-600">{project.description}</p>
            </div>
        </a>
        {/each}
    </div>

    <div class="mt-6 text-center">
        <a href="/projects" class="text-blue-600 hover:underline">
        View all projects →
        </a>
    </div>
</section>  