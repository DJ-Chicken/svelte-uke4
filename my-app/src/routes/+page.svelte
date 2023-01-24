<script>
    let counter = 0
    function increaseCounter(){
        counter += 1
    }
    function decreaseCounter(){
        counter -= 1
    }
</script>


<div>

    <h1> OVEN </h1>
    <p> Ovnen er {counter} grader </p>
    
    <button on:click={increaseCounter}> + </button>
    <button on:click={decreaseCounter}> - </button>

</div>