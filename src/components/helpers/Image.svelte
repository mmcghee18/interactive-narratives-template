<script>
	let { src, alt, caption } = $props();
</script>

<figure>
	<img {src} {alt} />

	{#if caption}
		<figcaption>{@html caption}</figcaption>
	{/if}
</figure>

<style>
	figure {
		width: 100%;
		height: 100%;
	}

	img {
		width: 100%;
		height: 100%;
		object-fit: cover;
	}

	figcaption {
		text-align: center;
		font-size: 14px;
		margin-top: 8px;
	}
</style>
