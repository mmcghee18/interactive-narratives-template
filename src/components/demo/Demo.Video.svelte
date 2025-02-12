<script>
	import Video from "$components/helpers/Video.svelte";
</script>

<div class="video-wrapper">
	<Video
		src="assets/demo/test.mp4"
		caption="Pass in different properties to customize the video, like looping and autoplay."
	/>
</div>

<style>
	.video-wrapper {
		height: 400px;
	}
</style>
