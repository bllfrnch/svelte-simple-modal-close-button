<script>
  import { getContext } from 'svelte';
  import CloseButton from './CloseButton.svelte';
  import Thing from './Thing.svelte';

  export let name;

  const { open } = getContext('simple-modal');
  const openModal = () => {
    open(Thing, { closeButton: CloseButton });
  };
</script>

<div>The name you entered is <button on:click={openModal}>{name}</button>.</div>