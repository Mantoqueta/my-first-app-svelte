<script lang="ts">
	 let name = 10;
	//  const add = () => {
	// 	name++;
	//  };
	//  const rest = () => {
	// 	name--;
	//  };
	//  const reser = () =>{
	// 	name = 0;
	//  }; 

	 const supreme = (value: number):number => (name += value);
	 const reset = (): number => (name = 0);
</script>

<main>
	<h1 class={ name < 0 ? "negative" : "positive"}>Hello {name}!</h1>
	<p>MIRA ES LA {new Date()}</p>
	<!-- <button class="add" on:click={add}>+1</button>
	<button class="rest" on:click={rest}>-1</button>
	<button class="reset" on:click={reser}>resetear</button>
	 -->
	<button class="add" on:click={() =>supreme(1)}>+1</button>
	<button class="rest" on:click={() =>supreme(-1)}>-1</button>
	<button class="reset" on:click={reset}>resetear</button>
</main>

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
	button:hover{
		cursor: pointer;
	}
	.add{
		background-color: green;
	}
	.rest{
		background-color: red;
	}
	.reset{
		background-color: yellow;
	}
	.negative{
		color:#ff3e00;
	}
	.positive{
		color: lime;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>