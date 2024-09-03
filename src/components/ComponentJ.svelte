<!-- src/components/ComponentJ.svelte -->
<script>
  import { onMount } from 'svelte';

  let timesMounted = 0;

  onMount(() => {
    timesMounted += 1;
  });
</script>

<h2 class="callout">Component J - Lifecycle Hooks Example</h2>
<p>Component has been mounted {timesMounted} {timesMounted === 1 ? 'time' : 'times'}.</p>
