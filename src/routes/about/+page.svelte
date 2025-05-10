<script>
	import headshot from '$lib/images/headshot-doge.jpg';
</script>

<svelte:head>
	<title>About | Rick Miskin</title>
  	<meta name="description" content="Learn more about Rick Miskin — a full-stack developer passionate about building great digital experiences." />
</svelte:head>

<section class="py-12 space-y-8 max-w-3xl mx-auto text-center">
  <h1 class="text-3xl font-bold">About Me</h1>

  <img
    src={headshot}
    alt="Rick Miskin headshot"
    class="mx-auto w-32 h-32 object-cover rounded-full border-4 border-blue-600"
  />

  <p class="text-lg text-gray-700">
    I'm Rick Miskin — a full-stack software engineer focused on building modern, responsive, and accessible websites. I collaborate with both employers and small businesses to create clean, fast solutions that solve real problems.
  </p>

  <p class="text-gray-600">
    I take pride in writing maintainable code, designing intuitive user interfaces, and delivering on time. When I'm not coding, I enjoy learning new technologies, helping others in the dev community, and contributing to open-source.
  </p>

  <div class="mt-6">
    <a
      href="/resume"
      class="bg-blue-600 text-white px-6 py-2 rounded-md hover:bg-blue-700 transition"
    >
      View Résumé
    </a>
  </div>
</section>