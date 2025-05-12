<script>
    import { onMount } from 'svelte';

    let joke = '';
    let isLoading = true;
    let error = null;

    // Fetch the joke from the API
    async function fetchJoke() {
        try {
            isLoading = true;
            const response = await fetch('https://icanhazdadjoke.com/', {
                headers: {
                    Accept: 'application/json'
                }
            });

            if (!response.ok) {
                throw new Error('Failed to fetch the joke');
            }

            const data = await response.json();
            joke = data.joke;
        } catch (err) {
            error = err.message;
        } finally {
            isLoading = false;
            
        }
    }

    // Fetch the joke when the component is mounted
    onMount(() => {
        fetchJoke();
    });
</script>

<svelte:head>
    <title>Dad Jokes - REST API Demo</title>
    <meta name="description" content="Learn how to call a REST API and display data dynamically using Svelte. This page fetches and displays a random dad joke from icanhazdadjoke.com." />
    <meta name="keywords" content="Svelte, REST API, Tailwind CSS, Dad Jokes, JavaScript, Web Development" />
    <meta name="author" content="Your Name" />
</svelte:head>

<div class="min-h-screen bg-gray-100 flex flex-col items-center justify-center p-4">
    <h1 class="text-4xl font-bold text-gray-800 mb-6">Random Dad Joke</h1>

    <div class="bg-white shadow-md rounded-lg p-6 max-w-md w-full">
        {#if isLoading}
            <p class="text-gray-500 text-center">Loading...</p>
        {:else if error}
            <p class="text-red-500 text-center">Error: {error}</p>
        {:else}
            <p class="text-lg text-gray-700 text-center">{joke}</p>
        {/if}
    </div>

    <button
        on:click={fetchJoke}
        class="mt-6 bg-blue-500 text-white px-4 py-2 rounded-lg shadow hover:bg-blue-600 transition"
    >
        Get Another Joke
    </button>
</div>