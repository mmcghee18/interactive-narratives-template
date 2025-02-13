<script>
	import DemoHero from "$components/demo/Demo.Hero.svelte";
	import DemoScrolly from "$components/demo/Demo.Scrolly.svelte";
	import DemoImages from "$components/demo/Demo.Images.svelte";
	import DemoVideo from "$components/demo/Demo.Video.svelte";

	/*
		This is a demonstration of all the helper components.
	*/
</script>

<div id="demo">
	<DemoHero />

	<div class="text">
		<p>Here are some examples of paragraphs.</p>

		<p>
			You should wrap your text in a container with a maximum height and the
			margin set to "0 auto". That way, it's centered on the screen and looks
			like a nice column.
		</p>

		<p>
			Here's a new paragraph. These p tags automatically have some space in
			between them. You can make some of your text <strong
				>bold, like this</strong
			>. Or italics, <i>like this</i>. Maybe you want to include a link to an
			external source, you could do that
			<a href="https://www.google.com/maps/">like this</a>.
		</p>

		<section>
			<DemoImages />
		</section>

		<section>
			<DemoVideo />
		</section>

		<section>
			<DemoScrolly />
		</section>
	</div>
</div>

<style>
	.text {
		max-width: 40rem;
		padding: 16px;
		margin: 0 auto;
	}

	section {
		margin: 32px auto;
		padding-top: 32px;
	}
</style>
