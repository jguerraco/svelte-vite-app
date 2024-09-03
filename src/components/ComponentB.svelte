<!-- src/components/ComponentB.svelte -->
<script>
  import moment from 'moment';

  let currentDate = moment().format('MMMM Do YYYY, h:mm:ss a');
</script>

<h2 class="callout">Component B - Moment.js Example</h2>
<p>{currentDate}</p>
