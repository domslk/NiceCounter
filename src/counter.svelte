<script>
    export let count;
</script>
<button on:click={() => {count += 1}}>count ++</button>

<style>
    button {
        background-color: red;
        border-color: red;
        color: white;
        
    }

    button:active {
        background-color: rgba(115, 0, 0, 0.718);
    }
    
</style>