<script>
    export let count = 0;
    function randomCount() {
        console.log(Math.random() * 2);
        if (Math.random() * 2 > 1) {
            count += Math.floor(Math.random() * 20);
        } else {
            count -= Math.floor(Math.random() * 20);
        }
    }
</script>

<main>
  <h1 class="m-10">Svelte + vite + Tailwindcss</h1>
    {#if count >= 0}
        <button class="bg-green-400 text-white focus:outline-none shadow-md shadow-slate-300 active:translate-y-2 active:shadow-none transition-all" on:click={randomCount}>Count: {count}</button>
    {:else}
        <button class="bg-rose-400 text-white focus:outline-none shadow-md shadow-slate-300 active:translate-y-2 active:shadow-none transition-all" on:click={randomCount}>Count: {count}</button>
    {/if}
</main>

<style>
</style>
