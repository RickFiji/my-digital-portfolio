<script>
  let name = '';
  let email = '';
  let message = '';
  let submitted = false;

  function handleSubmit(event) {
    event.preventDefault();
    submitted = true;
    // TODO: wire this up to Formspree, Resend, or your own endpoint
    console.log({ name, email, message });
  }
</script>

<svelte:head>
  <title>Contact | Rick Miskin</title>
  <meta name="description" content="Get in touch with Rick Miskin for freelance work, collaboration, or hiring inquiries." />
</svelte:head>

<section class="py-12 max-w-xl mx-auto space-y-8">
  <h1 class="text-3xl font-bold text-center">Contact Me</h1>
  <p class="text-center text-gray-600">
    Have a project in mind or just want to say hi? Fill out the form below and I’ll get back to you soon.
  </p>

  {#if submitted}
    <div class="text-green-600 font-semibold text-center">
      Thanks for your message! I’ll be in touch soon.
    </div>
  {:else}
    <form on:submit={handleSubmit} class="space-y-6">
      <div>
        <label for="name" class="block text-sm font-medium text-gray-700">Name</label>
        <input
          id="name"
          type="text"
          bind:value={name}
          required
          class="mt-1 w-full border px-3 py-2 rounded-md focus:outline-none focus:ring focus:border-blue-300"
        />
      </div>

      <div>
        <label for="email" class="block text-sm font-medium text-gray-700">Email</label>
        <input
          id="email"
          type="email"
          bind:value={email}
          required
          class="mt-1 w-full border px-3 py-2 rounded-md focus:outline-none focus:ring focus:border-blue-300"
        />
      </div>

      <div>
        <label for="message" class="block text-sm font-medium text-gray-700">Message</label>
        <textarea
          id="message"
          rows="5"
          bind:value={message}
          required
          class="mt-1 w-full border px-3 py-2 rounded-md focus:outline-none focus:ring focus:border-blue-300"
        ></textarea>
      </div>

      <div class="text-center">
        <button
          type="submit"
          class="bg-blue-600 text-white px-6 py-2 rounded-md hover:bg-blue-700 transition"
        >
          Send Message
        </button>
      </div>
    </form>
  {/if}
</section>