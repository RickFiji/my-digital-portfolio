<script>
    const year = new Date().getFullYear();
</script>
  
<footer class="mt-24 border-t pt-6 text-center text-sm">
    <p>© {year} Richard A Miskin II. All rights reserved.</p>
  
    <div class="mt-2">
      <a 
        href="https://www.patreon.com"
		target="_blank"
        aria-label="Support my work"
      >
        Support my work
      </a>
    </div>
</footer>
  
<style>
	p  {
		color: var(--color-text-grey);
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 12px;
	}
	footer {
		background-color: #f5f5f5;
	}
	footer a {
		font-weight: bold;
		color: var(--color-text-tertiary);
	}

	@media (min-width: 480px) {
		footer {
			padding: 12px 0;
		}
	}
</style>