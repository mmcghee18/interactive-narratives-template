<script>
	import Video from "$components/helpers/Video.svelte";

	/*
		Video is a component that creates a video.
		- src: The source of the video file.
		- caption: The caption for the video.
		- autoplay: Whether the video should autoplay.
		- loop: Whether the video should loop.
		- controls: Whether the video should have built-in controls (play, pause, etc).
	*/
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
