<script lang="ts">
  import { theme } from "../stores/theme";

  function toggleTheme() {
    theme.update((current) => (current === "light" ? "dark" : "light"));
  }
</script>

<svelte:head>
  <title>Home</title>
  <meta name="description" content="Svelte demo app" />
</svelte:head>

<section class="flex flex-col justify-center items-center w-full">
  <div class="w-10/12 h-full py-24 text-white">
    <div class="text-lg font-medium mb-2">Express freely what you feel;</div>
    <div
      class="text-6xl font-light md:w-[550px] w-full leading-[52px] nightshade"
    >
      Explore, Discover and write your own worst.
    </div>
    <div class="flex flex-row gap-4 mt-8">
      <a href="/confession">
        <button
          class="border-2 border-[#fffffff2] backdrop-blur hover:shadow rounded-tl-xl rounded-br-md px-6 py-2"
        >
          Explore
        </button>
      </a>
      <a href="/confess">
        <button
          class="border-2 border-[#fffffff2] backdrop-blur hover:shadow rounded-tl-xl rounded-br-md px-6 py-2"
        >
          Confess
        </button>
      </a>
    </div>
  </div>
</section>
