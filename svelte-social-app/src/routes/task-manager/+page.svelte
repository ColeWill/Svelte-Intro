<script>
	let count = 0;

	$: {
		if (count > 10) {
			console.log('I am the winner');
		}
	}
	$: doubled = count * 2;
</script>

<div class="text-white border-gray-100 p-2">
	<div>
		<p>I am the task manager page - {count}</p>
	</div>
	<div>
		<p>doubled value: {doubled}</p>
	</div>
	<button class="text-green-500 p-2" on:click={() => count++}>Increment</button>
	<button class="text-red-500 p-2" on:click={() => count--}>Decrement</button>
</div>
