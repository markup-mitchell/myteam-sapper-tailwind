<script>
  import { onMount } from "svelte";
  import { fade } from "svelte/transition";
</script>

<style>
div {
   position: relative;
}
</style>

{#if true}
<div in:fade="{{ duration: 200 }}">
  <slot><!-- optional fallback --></slot>
</div>
{/if}