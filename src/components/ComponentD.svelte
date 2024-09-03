<!-- src/components/ComponentD.svelte -->
<script>
  import { onMount } from 'svelte';
  import * as d3 from 'd3';

  let chart;

  onMount(() => {
    const data = [30, 80, 45, 60, 20, 90, 50];

    const svg = d3.select(chart)
      .append('svg')
      .attr('width', 300)
      .attr('height', 150);

    svg.selectAll('rect')
      .data(data)
      .enter()
      .append('rect')
      .attr('x', (d, i) => i * 35)
      .attr('y', d => 150 - d)
      .attr('width', 30)
      .attr('height', d => d)
      .attr('fill', 'teal');
  });
</script>

<h2 class="callout">Component D - D3.js Example</h2>
<div bind:this={chart}></div>
