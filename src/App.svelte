<script lang="ts">
    import Botao from "./components/Botao.svelte";
    import Calculadora from "./components/Calculadora.svelte";

</script>

<main>
	<Calculadora />

</main>

<style>
	:global(body){
		background-color: black;
	}
	:root{
		--back: #555;
	}
	main {
		display: flex;
		justify-content: center;
		align-items: center;
		height: 100vh;
	}


</style>