<!-- src/components/ComponentC.svelte -->
<script>
  import { onMount } from 'svelte';
  import axios from 'axios';

  let posts = [];

  onMount(async () => {
    try {
      const response = await axios.get('https://jsonplaceholder.typicode.com/posts');
      posts = response.data.slice(0, 5); // Only display the first 5 posts
    } catch (error) {
      console.error(error);
    }
  });
</script>

<h2 class="callout">Component C - Axios Example</h2>
<ul>
  {#each posts as post (post.id)}
    <li>{post.title}</li>
  {/each}
</ul>
