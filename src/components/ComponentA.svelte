<!-- src/components/ComponentA.svelte -->
<script>
  import { onMount } from 'svelte';
  import _ from 'lodash';

  let message = 'Hello Svelte';
  let reversedMessage = '';

  onMount(() => {
    reversedMessage = _.reverse([...message]).join('');
  });
</script>

<h2 class="callout">Component A - Lodash Example</h2>
<p>{reversedMessage}</p>
