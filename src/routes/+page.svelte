<script lang="ts">
	let count = 0;
	let name = '';

	function increment() {
		count++;
	}
</script>

<main class="mx-auto max-w-3xl p-6">
	<h1 class="mb-6 text-4xl font-bold">Learning Svelte</h1>

	<section class="mb-8">
		<h2 class="mb-4 text-2xl font-semibold">Interactive Examples</h2>

		<div class="space-y-6">
			<div class="rounded-lg bg-gray-100 p-4">
				<h3 class="mb-2 text-xl">1. Reactive State</h3>
				<button
					class="rounded bg-blue-500 px-4 py-2 text-white hover:bg-blue-600"
					on:click={increment}
				>
					Clicked {count}
					{count === 1 ? 'time' : 'times'}
				</button>
			</div>

			<div class="rounded-lg bg-gray-100 p-4">
				<h3 class="mb-2 text-xl">2. Two-way Binding</h3>
				<input
					type="text"
					bind:value={name}
					placeholder="Enter your name"
					class="rounded border p-2"
				/>
				{#if name}
					<p class="mt-2">Hello, {name}!</p>
				{/if}
			</div>
		</div>
	</section>

	<section class="mb-8">
		<h2 class="mb-4 text-2xl font-semibold">Key Resources</h2>
		<ul class="list-disc space-y-2 pl-6">
			<li>
				<a href="https://svelte.dev/tutorial" class="text-blue-600 hover:underline" target="_blank">
					Interactive Tutorial
				</a>
				- Learn Svelte step by step
			</li>
			<li>
				<a href="https://svelte.dev/docs" class="text-blue-600 hover:underline" target="_blank">
					Documentation
				</a>
				- Complete Svelte reference
			</li>
			<li>
				<a
					href="https://kit.svelte.dev/docs/introduction"
					class="text-blue-600 hover:underline"
					target="_blank"
				>
					SvelteKit Docs
				</a>
				- Full-stack Svelte framework
			</li>
		</ul>
	</section>

	<section>
		<h2 class="mb-4 text-2xl font-semibold">Why Svelte?</h2>
		<ul class="list-disc space-y-2 pl-6">
			<li>Write less code with a clean, intuitive syntax</li>
			<li>True reactivity built into the language</li>
			<li>No virtual DOM - compiles to vanilla JavaScript</li>
			<li>Built-in animations and transitions</li>
			<li>Small bundle sizes for better performance</li>
		</ul>
	</section>
</main>

<style>
	:global(body) {
		margin: 0;
		padding: 0;
	}
</style>
