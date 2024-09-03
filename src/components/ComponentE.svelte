<!-- src/components/ComponentE.svelte -->
<script>
  let name = '';
</script>

<h2 class="callout">Component E - Reactive Input Example</h2>
<input bind:value={name} placeholder="Enter your name" />
<p>Hello, {name}</p>
