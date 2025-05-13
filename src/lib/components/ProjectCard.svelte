<script>
    export let title;
    export let description;
    export let image;
    export let url;
</script>
  
<a
    href={url}
    target="_blank"
    rel="noopener noreferrer"
    class="block border rounded overflow-hidden hover:shadow-lg transition bg-white"
>
    <img src={image} alt={title} class="w-full h-48 object-cover" />
    <div class="p-4">
      <h2 class="text-center text-xl font-semibold">{title}</h2>
      <p class="text-center text-gray-600">{description}</p>
    </div>
</a>
<style>
    p {
        text-decoration: none;
        color: rgb(91, 91, 91);
    }
</style>
  