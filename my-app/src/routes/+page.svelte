<script>
    
    let counter = 0;
	let holdingDown = false;

	function increment() {
		counter++;
		if (holdingDown) {
			setTimeout(increment, 15);
		}
	}
    function decrement() {
        if (counter > 0) {
            counter--;
            if (holdingDown) {
                setTimeout(decrement, 15);
            }   
        }
	}

</script>


<div class="flex min-h-screen justify-center items-center w-full">
    <div class="flex justify-center items-center max-w-xs w-full">
        
        <button on:pointerdown={() => {
            holdingDown = true; decrement();
        }} on:pointerup={() => (holdingDown = false)} class="flex justify-center items-center w-9 h-9 border rounded-full m-auto"> - </button>

        <p class="flex justify-center items-center w-3/5 "> {counter}° </p>
        
        <button on:pointerdown={() => {
            holdingDown = true; increment();
        }} on:pointerup={() => (holdingDown = false)} class="flex justify-center items-center w-9 h-9 border rounded-full m-auto"> + </button>
    
    
    </div>
</div>
