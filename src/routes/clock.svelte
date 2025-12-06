<script lang="ts">
	import { onMount, onDestroy } from 'svelte';
	let intervalId: ReturnType<typeof setInterval>;
	let time = $state(0);
	const updateTime = () => {
		time++;
	};
	onMount(() => {
		intervalId = setInterval(() => {
			updateTime();
		}, 1000);
		console.log(`mounted at time = ${$state.snapshot(time)}`);
	});

	onDestroy(() => {
		clearInterval(intervalId);
		console.log(`unmounted at time = ${$state.snapshot(time)}`);
	});
</script>

<h1>time: {time} seconds</h1>
