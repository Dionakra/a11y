<script lang="ts">
	import crossmark from "$lib/images/crossmark.svg";
	import checkmark from "$lib/images/checkmark.svg";
	import { base } from "$app/paths";
</script>

<svelte:head>
	<title>Accesibilidad - Una cuestión de UX</title>
	<meta
		name="description"
		content="Web que muestra dos páginas idénticas en interfaz, pero diferente en cuanto a usabilidad debido a la accesibilidad"
	/>
</svelte:head>

<section>
	<div class="text-center py-12 mb-8">
		<h1 class="text-3xl">Comparativa de UX basada en Accesibilidad</h1>

		<h2 class="text-xl text-gray-800 pt-2">
			Ejemplos realizados usando <strong>Svelte</strong> y
			<strong>TailwindCSS</strong>
		</h2>
	</div>

	<div class="flex justify-center gap-x-24 text-xl">
		<a
			aria-label="Enlace a ejemplo de web incorrecta en términos de accesibilidad"
			href="{base}/incorrect"
			class="flex items-center justify-center h-full bg-white w-1/3 max-w-64 max-h-64 aspect-square rounded-md shadow-md cursor-pointer hover:shadow-red-300 hover:shadow-lg"
		>
			<div class="px-4">
				<div class="break-words text-3xl text-center mb-4">
					Mala Accesibilidad
				</div>
				<div class="flex justify-center">
					<img
						class="h-12"
						src={crossmark}
						alt="Imagen con una cruz roja"
					/>
				</div>
			</div>
		</a>
		<a
			aria-label="Enlace a ejemplo de web correcta en términos de accesibilidad"
			href="{base}/correct"
			class="flex items-center justify-center h-full bg-white w-1/3 max-w-64 max-h-64 aspect-square rounded-md shadow-md cursor-pointer hover:shadow-blue-300 hover:shadow-lg"
		>
			<div class="px-4">
				<div class="break-words text-3xl text-center mb-4">
					Buena Accesibilidad
				</div>
				<div class="flex justify-center">
					<img
						class="h-12"
						src={checkmark}
						alt="Imagen con un tick azul "
					/>
				</div>
			</div>
		</a>
	</div>
</section>

<style>
</style>
