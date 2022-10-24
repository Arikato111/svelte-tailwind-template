<script>
  import { isDark } from "./CheckMode";
  let Text = isDark() ? "🌚" : "🌞";

  function changeMode() {
    let state = window.document.documentElement.classList.contains("dark");
    if (state) {
      window.document.documentElement.classList.remove("dark");
      Text = "🌞";
    } else {
      window.document.documentElement.classList.add("dark");
      Text = "🌚";
    }
  }
</script>

<svelte:window />

<div class="absolute top-0 right-0 text-5xl p-2">
  <button on:click={changeMode}>
    {Text}
  </button>
</div>
