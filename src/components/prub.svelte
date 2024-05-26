<script>
  let count = 1;

  // the `$:` means 're-run whenever these values change'
  $: doubled = count * 2;
  $: quadrupled = doubled * 2;

  function handleClick() {
    count += 1;
  }

  let user = { loggedIn: false };

  function toggle() {
    user.loggedIn = !user.loggedIn;
  }
</script>


<section class="container  text-center">
	{#if user.loggedIn}
	  <button on:click={toggle}> Log out </button>
	{:else}
	  <button on:click={toggle}> Log in </button>
	{/if}
	</section>
	
	
	<section class="container text-center">
	<button 
	  on:click={handleClick}
	  type="button"
	  class="text-gray-900 bg-gradient-to-r from-lime-200 via-lime-400 to-lime-500 hover:bg-gradient-to-br focus:ring-4 focus:outline-none focus:ring-lime-300 dark:focus:ring-lime-800 font-medium rounded-lg text-sm px-5 py-2.5 text-center me-2 mb-2"
	>
	  Count: {count}
	</button>
	
	<p>{count} * 2 = {doubled}</p>
	<p>{doubled} * 2 = {quadrupled}</p>
	</section>