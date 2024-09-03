<!-- src/components/ComponentI.svelte -->
<script>
  import ChildComponent from './ChildComponent.svelte';

  let message = '';

  function receiveMessage(event) {
    message = event.detail;
  }
</script>

<h2 class="callout">Component I - Parent-Child Communication Example</h2>
<ChildComponent on:message-from-child={receiveMessage} />
<p>{message}</p>
