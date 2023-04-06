<script lang="ts">
    export let texto: string;
    export let triplo: boolean = false;
    export let duplo: boolean = false;
    export let op: boolean = false;
    export let destaque: boolean = false;
    export let onClick: (valor: string) => void = () => {}

</script>

<button 
    on:click={()=>onClick(texto)}
    class="botao" class:triplo class:duplo class:op class:destaque >
    {texto}
</button>

<style>
.botao{
    margin: 0;
    border: 1px solid var(--back);
    flex-basis: 25%;
}
.duplo{
    flex-basis: 50%;
}
.triplo{
    flex-basis: 75%;
}
.op{
    background-color: chocolate;
    color: white;
}
.destaque{
    background-color: red;
    color: white;
}
</style>