<script>
	const { hed, dek, byline, src, alt } = $props();
</script>

<div class="hero">
	{#if src.endsWith(".mp4")}
		<video {src} autoplay loop muted playsinline></video>
	{:else}
		<img {src} {alt} />
	{/if}

	<div class="text">
		{#if hed}<h1>{@html hed}</h1>{/if}
		{#if dek}<h2>{@html dek}</h2>{/if}
		{#if byline}<p>{@html byline}</p>{/if}
	</div>
</div>

<style>
	.hero {
		width: 100vw;
		height: 100vh;
		position: relative;
	}

	img,
	video {
		height: 100%;
		width: 100%;
		object-fit: cover;
	}

	.text {
		position: absolute;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);
		color: white;
		background: rgba(0, 0, 0, 0.5);
		padding: 0 1rem;
		text-align: center;
	}
</style>
