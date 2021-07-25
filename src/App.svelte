<script>
  import './styles.css'
  import { onMount } from 'svelte'
  import { getWelcomeMessage } from './util'

  onMount(() => {
    console.log(getWelcomeMessage())
  })
</script>

<main class="dark:bg-black h-screen w-screen flex flex-col items-center justify-center fixed">
  <div class="flex flex-col gap-6">
    <h1 class="text">
      <span class="text-green-500">V</span><span class="text-gray-400 text-opacity-50">ite</span>
    </h1>
    <h1 class="text">
      <span class="text-yellow-500">S</span><span class="text-gray-400 text-opacity-50">velte</span>
    </h1>
    <h1 class="text">
      <span class="text-blue-400">T</span><span class="text-gray-400 text-opacity-50">ailwind</span>
    </h1>
    <h1 class="text">
      <span class="text-blue-600">T</span><span class="text-gray-400 text-opacity-50">ypeScript</span>
    </h1>
  </div>
</main>

<style lang="postcss">

  .text {
    @apply text-5xl md:text-8xl font-mono select-none;
  }

</style>