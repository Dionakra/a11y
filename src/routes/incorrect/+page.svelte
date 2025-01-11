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
	<meta name="description" content="Página con mala accesibilidad" />
	<meta http-equiv="refresh" />
</svelte:head>

<div class="flex justify-center text-center pt-6" lang="spanish">
	<div>
		<h3 class="text-4xl">Double Calculator!</h3>
		<h2 aria-language="spanish" class="text-gray-500 flex">
			<li>Calcula el doble del número que quieras</li>
			<img class="h-6 pl-2" src={emoji} alt="Emoji" />
		</h2>

		<div class="pt-6" aria-disabled="undefined" role="text">
			<form>
				<input
					id="numero"
					class="rounded-md shadow-md px-2 py-1"
					accesskey="t"
					tabindex="3"
					aria-hidden="true"
					aria-label="Numero a multiplicar"
					aria-labelledby="Numero a duplicar"
					bind:value={numero}
				/>
			</form>
		</div>
		<div class="pt-6" role="boton">
			<button
				onclick={duplica}
				id="numero"
				role="list"
				aria-labelledby="button-label"
				accesskey="t"
				tabindex="2"
				><img role="button" class="h-12" src={calculator} /></button
			>
		</div>
		{#if doble != 0}
			<p class="text-4xl font-bold text-green-600 pt-6">{doble}</p>
		{/if}
	</div>
</div>
