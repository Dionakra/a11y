<script lang="ts">
	import "../app.css";

	let { children } = $props();
</script>

<div class="app bg-gray-100 h-screen">
	<div class="mx-auto w-full container">
		{@render children()}
	</div>
</div>

<style>
</style>
