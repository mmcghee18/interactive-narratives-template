<script>
	import Image from "$components/helpers/Image.svelte";

	/*
		The Image component creates an image with an optional caption.
		- src: The source of the image file.
		- alt: The alt text for the image.
		- caption: The caption for the image.
		
		The image will take on the width and height of its container. To make the image smaller or larger,
		wrap it in a container of the size you want.
	*/
</script>

<Image
	src="assets/demo/test.jpg"
	alt="A lake and some clouds"
	caption="This is a caption"
/>

<div class="small">
	<Image
		src="assets/demo/test.jpg"
		alt="A lake and some clouds"
		caption="The image will fill the width and height of its container"
	/>
</div>

<div class="grid">
	{#each [1, 2, 3, 4] as i}
		<Image src="assets/demo/test.jpg" alt="A lake and some clouds" />
	{/each}
</div>

<style>
	.small {
		width: 300px;
		margin: 36px auto;
	}

	.grid {
		display: grid;
		grid-template-columns: repeat(2, 1fr);
		gap: 16px;
	}
</style>
