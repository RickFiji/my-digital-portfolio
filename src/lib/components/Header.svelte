<script>
  import { page } from '$app/stores';

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
    <a href="/" class="text-xl font-bold text-blue-700">
      Rick Miskin
    </a>

    <div class="flex space-x-4 text-sm sm:text-base">
      {#each links as { href, label }}
        <a
          href={href}
          class="text-gray-700 hover:text-blue-600 transition"
          class:selected={$page.url.pathname === href}
        >
          {label}
        </a>
      {/each}
    </div>
  </div>
</nav>

<style>
  a.selected {
    font-weight: bold;
    color: #1d4ed8; /* Tailwind blue-700 */
  }
</style>