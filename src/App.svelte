<script lang="ts">
  import ToggleMode from "./components/ToggleMode.svelte";
  import Footer from "./components/Footer.svelte";
  import { checkTheme } from "./components/CheckMode";
  checkTheme();

  export let count: number = 0;
  function randomCount(): void {
    if (Math.random() * 2 > 1) {
      count += Math.floor(Math.random() * 20);
    } else {
      count -= Math.floor(Math.random() * 20);
    }
  }
</script>

<main class="main-screen">
  <ToggleMode />
  <h1 class="p-10 text-2xl sm:text-4xl title">Svelte + vite + Tailwindcss</h1>
  {#if count >= 0}
    <button class="btn bg-green-400 dark:bg-green-600 dark:hover:bg-green-500" on:click={randomCount}>Count: {count}</button>
  {:else}
    <button class="btn bg-rose-400 dark:bg-rose-600 dark:hover:bg-rose-500" on:click={randomCount}>Count: {count}</button>
  {/if}
</main>
<Footer />

<style>
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
