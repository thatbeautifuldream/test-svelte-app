<script lang="ts">
	let count = 0;

	function increment() {
		count += 1;
	}

	function decrement() {
		count -= 1;
	}

	function reset() {
		count = 0;
	}
</script>

<div class="flex flex-col items-center gap-4 p-4">
	<h1 class="text-2xl font-bold">Counter App</h1>

	<div class="text-4xl font-bold">{count}</div>

	<div class="flex gap-2">
		<button class="rounded bg-blue-500 px-4 py-2 text-white hover:bg-blue-600" on:click={increment}>
			Increment
		</button>

		<button class="rounded bg-red-500 px-4 py-2 text-white hover:bg-red-600" on:click={decrement}>
			Decrement
		</button>

		<button class="rounded bg-gray-500 px-4 py-2 text-white hover:bg-gray-600" on:click={reset}>
			Reset
		</button>
	</div>
</div>
