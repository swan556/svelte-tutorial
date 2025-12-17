<script lang="ts">
</script>

<button class="object" onkeypress={(key) => console.log('pressed', key)}> hello </button>

<style>
	:global(body) {
		height: 100dvh;
		width: 100dvw;
		background-color: rgb(58, 58, 58);
		display: flex;
		justify-content: center;
		align-items: center;
	}
	.object {
		width: 200px;
		height: 100px;
		background-color: grey;
	}
</style>
