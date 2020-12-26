<script lang="ts">
  import Nav from '../components/Nav.svelte';

  export let segment: string;
</script>

<style global lang="postcss">
@tailwind base;
@tailwind components;
@tailwind utilities;

</style>

<Nav segment="{segment}" />

<main class="grid mx-auto max-w-screen-xl p-6 text-gray-800">
  <slot />
</main>
