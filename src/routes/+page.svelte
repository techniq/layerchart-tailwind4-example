<script lang="ts">
	import '../app.css';
	import { AreaChart } from 'layerchart';
	import { data } from './data';
</script>

<main class="p-10">
	<div class="h-[300px] p-4 border rounded">
		<!-- Need to override `hsl(var(--color-primary))` since you define CSS color variables with colorspace functions in Tailwind 4 -->
		<AreaChart
			{data}
			x="date"
			y="value"
			series={[{ key: 'value', color: 'var(--color-primary)' }]}
		/>
	</div>
</main>
