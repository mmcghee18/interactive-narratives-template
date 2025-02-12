<script>
	const {
		src,
		caption,
		loop = false,
		autoplay = false,
		controls = true
	} = $props();
</script>

<figure>
	<video {src} {loop} {autoplay} {controls} playsinline></video>

	{#if caption}
		<figcaption>{@html caption}</figcaption>
	{/if}
</figure>

<style>
	figure {
		width: 100%;
		height: 100%;
	}

	video {
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
