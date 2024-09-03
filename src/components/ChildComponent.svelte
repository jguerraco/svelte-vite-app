<!-- src/components/ChildComponent.svelte -->
<script>
  import { createEventDispatcher } from 'svelte';

  const dispatch = createEventDispatcher();

  function sendMessage() {
    dispatch('message-from-child', 'Hello from Child');
  }
</script>

<button on:click={sendMessage}>Send Message to Parent</button>
