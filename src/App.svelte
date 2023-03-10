<div>

  <h1>Hola, {nome}</h1>

  <input type="text" bind:value={nome}>
  <p>{nome}</p>

  <input type="text" bind:value={apelidos} >
  <p>{apelidos}</p>

  <p>{nomeCompleto}</p>

  <button on:click={manexadorMostrar}>Mostrar?</button>

  {#if (mostrar)}
    <Componente propiedade={0}/>
  {/if}

</div>

<script>
  import Componente from "./Componente.svelte";

  let nome = "Daniel"
  let apelidos = "Bañobre"
  let nomeCompleto
  let mostrar = true

  function manexadorMostrar() {
    mostrar = !mostrar
  }

  $: {
    nomeCompleto = `-> ${nome} ${apelidos}.`
  } 
</script>
