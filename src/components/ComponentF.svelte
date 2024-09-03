<!-- src/components/ComponentF.svelte -->
<script>
  let showMessage = false;

  function toggle() {
    showMessage = !showMessage;
  }
</script>

<h2 class="callout">Component F - Conditional Rendering Example</h2>
<button on:click={toggle}>Toggle Message</button>
{#if showMessage}
  <p>You toggled me!</p>
{/if}
