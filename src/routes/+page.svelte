<script lang="ts">
	import Clock from './clock.svelte';
	let showclock = $state(true);
</script>

{#if showclock}
	<Clock />
{/if}

<button
	onclick={() => {
		showclock = !showclock;
	}}
>
	show/hide clock
</button>
