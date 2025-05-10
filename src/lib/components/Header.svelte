<script>
  import { page } from '$app/stores';
  let menuOpen = false;

  const links = [
    { href: '/', label: 'Home' },
    { href: '/projects', label: 'Projects' },
    { href: '/about', label: 'About' },
    { href: '/resume', label: 'Résumé' },
    { href: '/contact', label: 'Contact' }
  ];
</script>

<nav class="bg-white border-b px-4 py-4">
  <div class="max-w-7xl mx-auto flex justify-between items-center">
    <!-- Logo -->
    <a href="/" class="text-xl font-bold text-blue-700">
      Rick Miskin
    </a>

    <!-- Desktop Nav -->
    <div class="hidden sm:flex space-x-6">
      {#each links as { href, label }}
        <a
          href={href}
          class="text-gray-700 hover:text-blue-600 transition font-medium"
          class:selected={$page.url.pathname === href}
        >
          {label}
        </a>
      {/each}
    </div>

    <!-- Mobile Menu Button -->
    <button
      class="sm:hidden text-gray-700 focus:outline-none"
      on:click={() => (menuOpen = !menuOpen)}
      aria-label="Toggle navigation"
    >
      <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
        {#if menuOpen}
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
        {:else}
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
        {/if}
      </svg>
    </button>
  </div>

  <!-- Mobile Nav Links -->
  {#if menuOpen}
    <div class="sm:hidden flex flex-col mt-4 space-y-2">
      {#each links as { href, label }}
        <a
          href={href}
          class="px-4 py-2 text-gray-700 hover:text-blue-600 font-medium"
          class:selected={$page.url.pathname === href}
        >
          {label}
        </a>
      {/each}
    </div>
  {/if}
</nav>

<style>
  a.selected {
    font-weight: bold;
    color: #1d4ed8;
  }
</style>
