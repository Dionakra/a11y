<script>
	import calculator from "$lib/images/x2.svg";
	import emoji from "$lib/images/emoji.svg";

	let doble = $state(0);
	let numero = $state(0);

	function duplica() {
		doble = numero * 2;
	}
</script>

<svelte:head>
	<title>Ejemplo correcto de accesibilidad</title>
	<meta name="description" content="Página con mala accesibilidad" />
</svelte:head>

<div class="flex justify-center text-center pt-6">
	<div>
		<h1 class="text-4xl">Double Calculator!</h1>
		<h2 class="text-gray-600 flex">
			<p>Calcula el doble del número que quieras</p>
			<img class="h-6 pl-2" src={emoji} alt="Emoji" />
		</h2>

		<div class="pt-6">
			<input
				aria-label="Número a duplicar"
				class="rounded-md shadow-md px-2 py-1"
				bind:value={numero}
			/>
		</div>
		<div class="pt-6">
			<button onclick={duplica} aria-label="Duplicar número"
				><img
					class="h-12"
					src={calculator}
					alt="Duplica el número!"
				/></button
			>
		</div>
		{#if doble != 0}
			<p class="text-4xl font-bold text-green-600 pt-6">{doble}</p>
		{/if}
	</div>
</div>
