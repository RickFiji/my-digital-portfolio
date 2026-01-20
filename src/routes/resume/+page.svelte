<script>
  const resumeUrl = '/resume.pdf'; // Static import to your PDF resume from /static/resume.pdf
</script>

<svelte:head>
  <title>Résumé | Rick Miskin</title>
  <meta name="description" content="View and download the résumé of Rick Miskin, full-stack software engineer." />
</svelte:head>

<section class="py-12 space-y-8 max-w-3xl mx-auto">
  <h1 class="text-3xl font-bold text-center">Résumé</h1>

  <div class="text-center">
    <a
      href={resumeUrl}
      download
      class="inline-block bg-blue-600 text-white px-6 py-2 rounded-md hover:bg-blue-700 transition"
    >
      Download PDF
    </a>
  </div>

  <!-- Inline résumé content -->
  <div class="space-y-6 mt-8">
    <section>
      <h2 class="text-xl font-semibold text-blue-700">Experience</h2>
      <ul class="mt-2 text-gray-700 space-y-4">
        <li>
          <strong>Sr. Software Engineer</strong> — (2025–Present)<br />
          Built and maintained websites using Svelte, React, and custom CMS integrations.
        </li>
        <li>
          <strong>Product Owner</strong> — (2025)<br />
          Built and maintained websites for local businesses using Svelte, React, and custom CMS integrations.
        </li>
        <li>
          <strong>Software Engineer</strong> — Example Corp (2014–2025)<br />
          Developed scalable applications using .NET Core and modern JavaScript frameworks. Led small teams and mentored junior developers.
        </li>
      </ul>
    </section>

    <section>
      <h2 class="text-xl font-semibold text-blue-700">Skills</h2>
      <p class="text-gray-700">JavaScript, Svelte, SvelteKit, .NET, SQL, Tailwind CSS, REST APIs, Git, CI/CD, Agile</p>
    </section>

    <section>
      <h2 class="text-xl font-semibold text-blue-700">Education</h2>
      <p class="text-gray-700">
        B.S. in Computer Science — Appalachain State University<br />
        Graduated 2014
      </p>
    </section>
  </div>
</section>