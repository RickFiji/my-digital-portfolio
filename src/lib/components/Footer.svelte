<script>
    const year = new Date().getFullYear();
</script>
  
<footer class="mt-24 border-t pt-6 text-center text-sm text-gray-500">
    <p>© {year} Richard A Miskin II. All rights reserved.</p>
  
    <div class="mt-2">
      <a 
        href="https://www.patreon.com"
		target="_blank"
        class="text-blue-600 hover:underline"
        aria-label="Support my work"
      >
        Support my work
      </a>
    </div>
</footer>
  
<style>    
	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 12px;
	}

	footer a {
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 12px 0;
		}
	}
</style>