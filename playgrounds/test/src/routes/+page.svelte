<script>
	let items = []
</script>

<button on:click={()=> items = [...items, items.length]}>Add Item</button>

{#each items as item, i}
<div class="card">
	{i}
</div>
{/each}

<style>
	@starting-style{
		.card{
			opacity: 0;
			height: 0;
		}
	}	
	.card {
		background-color: orange;
		max-width: max-content;
		padding: 1rem;
		border-radius: 1rem;
		display: grid;
		margin: auto;
		transform-origin: bottom;
		overflow: hidden;
		transition: opacity 1s, display 1s, height 1s;
		transition-behavior: allow-discrete;
	}
</style>