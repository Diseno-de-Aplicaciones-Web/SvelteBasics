<div>
    <p>O valor da propiedade é {propiedade}</p>
    <button on:click={manexadorClick}>+</button>
</div>

<script>
    export let propiedade
    function manexadorClick(){
        propiedade++
    }
</script>