<script>
	import Scrolly from "$components/helpers/Scrolly.svelte";

	let value = $state();

	const explanation = [
		"Scrollytelling is a great technique for telling stories with scrolling.",
		"Everything in the container with class 'sticky' will stay put, while these steps scroll over it.",
		"You could put images, videos, charts, or anything in that 'sticky' container.",
		"You can have it update based on what step we're on, which is tracked in the variable called value.",
		"Have fun!"
	];
</script>

<section id="scrolly">
	<div class="sticky">
		<h2>Current scroll step: <span>{value}</span></h2>
	</div>

	<div class="spacer"></div>

	<Scrolly bind:value>
		{#each explanation as text, i}
			{@const active = value === i}
			<div class="step" class:active>
				<p>{text}</p>
			</div>
		{/each}
	</Scrolly>

	<div class="spacer"></div>
</section>

<style>
	.sticky {
		position: sticky;
		top: 4em;
	}

	.spacer {
		height: 75vh;
	}

	.step {
		margin: 80vh 0;
		background: var(--color-gray-100);
		text-align: center;
	}

	.step p {
		padding: 1rem;
	}

	span {
		background: var(--color-mark);
		padding: 0 8px;
	}
</style>
