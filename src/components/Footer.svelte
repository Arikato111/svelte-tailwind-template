<script>
  import GithubIcons from "./icons/GithubIcons.svelte";
</script>

<footer>
  <div class="absolute left-0 bottom-0 m-2 py-1 px-2 rounded bg-yellow-200">
    <a href="/#">other button</a>
  </div>
  <div class="absolute right-0 bottom-0 inline-block m-2 ">
    <a
      target="_blank"
      title="view source code"
      rel="noreferrer"
      href="https://github.com/Arikato111/svelte-tailwind-template"
    >
      <!-- <img class="w-12" src="/github.png" alt="github icon" /> -->
      <div
        class="inline-block fill-black dark:fill-white w-14 shadow-md shadow-gray-600 rounded-full"
      >
        <GithubIcons />
      </div>
    </a>
  </div>
</footer>
