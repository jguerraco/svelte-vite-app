<!-- src/components/ComponentG.svelte -->
<script>
  let items = ['Item 1', 'Item 2', 'Item 3', 'Item 4'];
</script>

<h2 class="callout">Component G - List Rendering Example</h2>
<ul>
  {#each items as item}
    <li>{item}</li>
  {/each}
</ul>
