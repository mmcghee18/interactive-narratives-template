<script>
	import Image from "$components/helpers/Image.svelte";
</script>

<section>
	<Image
		src="assets/demo/test.jpg"
		alt="A lake and some clouds"
		caption="Look at this beautiful lake!"
	/>
</section>

<section>
	<div class="small">
		<Image
			src="assets/demo/test.jpg"
			alt="A lake and some clouds"
			caption="The image will fill the width and height of its container"
		/>
	</div>
</section>

<section>
	<div class="grid">
		{#each [1, 2, 3, 4] as i}
			<Image src="assets/demo/test.jpg" alt="A lake and some clouds" />
		{/each}
	</div>
</section>

<style>
	.small {
		width: 300px;
		margin: 0 auto;
	}

	.grid {
		display: grid;
		grid-template-columns: repeat(2, 1fr);
		gap: 16px;
	}
</style>
