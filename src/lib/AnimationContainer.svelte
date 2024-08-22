<script lang="ts">
	import { fade } from 'svelte/transition';
</script>


<div
	in:fade={{ duration: 300, delay: 300 }}
	out:fade={{ duration: 300 }}
	style="grid-row: 1 / -1; grid-column: 1 / -1; display: grid; gap: 20px;"
>
	<slot />
</div>
