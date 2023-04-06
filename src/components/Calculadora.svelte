<script lang="ts">
	import Tela from './Tela.svelte';
    import Botao from "./Botao.svelte";
    import Linha from "./Linha.svelte";
    
    let valor = '0';



    function numeroDigitado(numero: string){
        valor += numero
    }

</script>

<div class="calculadora">
    <Tela valor = {valor}/>
    <Linha>
        <Botao texto="AC" triplo destaque />
        <Botao texto="/" op />
        
    </Linha>
    <Linha>
        <Botao texto="7" onClick={numeroDigitado}/>
        <Botao texto="8" onClick={numeroDigitado}/>
        <Botao texto="9" onClick={numeroDigitado}/>
        <Botao texto="*" op/>
    </Linha>
    <Linha>
        <Botao texto="6" />
        <Botao texto="5" />
        <Botao texto="4" />
        <Botao texto="+" op/>
    </Linha>
    <Linha>
        <Botao texto="1" />
        <Botao texto="2" />
        <Botao texto="3" />
        <Botao texto="-" op/>
    </Linha>
    <Linha>
        <Botao texto="0" duplo/>
        <Botao texto="," />
        <Botao texto="=" destaque/>
    </Linha>
</div>

<style>
    .calculadora {
        height: 220px;
        width: 150px;
        padding: 10px;
        border-radius: 10px;
        background-color: var(--back);

        display: flex;
        flex-direction: column;
    }
</style>
