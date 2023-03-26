<script>
	let name = 'world';
	let myflavor;
	let bought = false;
	let flavors = 	['strawberry','chocolate','vanilla','lime'];
	function buyIcecream(){
		  bought = true;	  
	}
</script>

{#if bought}
<p>
	You have bought {myflavor}
</p>
{:else}
	Please choose any flavor!<br><br>
<select bind:value={myflavor}>
	{#each flavors as flavor}
	<option value={flavor}>{flavor} flavor</option>
	{/each}
</select>
<button on:click={buyIcecream}>
	Buy
</button>
{/if}
