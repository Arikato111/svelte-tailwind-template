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

<main class="border-4 border-green-400">
  <h1 class="p-10 text-4xl title">Svelte + vite + Tailwindcss</h1>
  {#if count >= 0}
    <button
      class="bg-green-400 p-2 rounded text-white focus:outline-none shadow-md shadow-slate-300 active:translate-y-2 active:shadow-none transition-all"
      on:click={randomCount}>Count: {count}</button
    >
  {:else}
    <button
      class="bg-rose-400 p-2 rounded text-white focus:outline-none shadow-md shadow-slate-300 active:translate-y-2 active:shadow-none transition-all"
      on:click={randomCount}>Count: {count}</button
    >
  {/if}
</main>

<style>
  main {
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    box-sizing: border-box;
  }
  .title {
    animation: roling ease 10s infinite;
  }
  @keyframes roling {
    0% {
      transform: rotate(10deg);
    }
    50% {
      transform: rotate(-10deg);
    }
    100% {
      transform: rotate(10deg);
    }
  }
</style>
