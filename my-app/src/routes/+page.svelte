<script>
    let counter = 0


    function increaseCounter(){
        counter += 1
    }
    function decreaseCounter(){
        if (counter > 0) {
            counter -= 1
        }
    }
    
</script>


<div class="flex min-h-screen justify-center items-center w-full">
    <div class="flex justify-center items-center max-w-xs w-full">
        <button on:click={increaseCounter} class="flex justify-center items-center w-9 h-9 border rounded-full m-auto"> + </button>
        <p class="flex justify-center items-center w-3/5 "> {counter}° </p>
        <button on:click={decreaseCounter} class="flex justify-center items-center w-9 h-9 border rounded-full m-auto"> - </button>
    </div>
</div>