<!-- src/components/ComponentH.svelte -->
<script>
  let num = 0;

  // Reactive statement to compute the square
  $: square = num * num;
</script>

<h2>Component H - Computed Property Example</h2>
<input type="number" bind:value={num} />
<p>Square of {num} is {square}</p>
