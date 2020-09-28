<script>
	import Modal from 'svelte-simple-modal';
	import Child from './Child.svelte';
  export let name = 'World';
</script>

<Modal>
	<main>
		<label>
			Name:
			<input bind:value={name} />
		</label>
		<h1>Hello {name}!</h1>
		<Child {name} />
	</main>
</Modal>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}
</style>