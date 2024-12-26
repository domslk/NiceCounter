<script>
    export let count;
</script>
<button on:click={() => {count += 1}}></button>

<style>
    button {
        background-color: rgba(255, 0, 0, 0);
        border: 0;
        color: white;
        display: block;
        width: 100%;
        height: 100%;
        transition: background 0.6s;
    }

    button:active {
        background-color: rgba(139, 0, 0, 0.165);
        animation: wiggle 2.5s infinite;
        transition: background 0s;
    }
    
</style>