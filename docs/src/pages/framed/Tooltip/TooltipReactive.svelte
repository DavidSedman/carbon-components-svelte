<script>
  import { Tooltip, Button } from "carbon-components-svelte";

  let open = true;
</script>

<style>
  div {
    margin-top: var(--cds-spacing-05);
  }
</style>

<Tooltip bind:open triggerText="Resource list" align="start">
  <p>Resources are provisioned based on your account's organization.</p>
</Tooltip>

<div style="margin-top: var(--cds-spacing-12);">
  <Button size="small" on:click="{() => (open = !open)}">
    {open ? 'Close tooltip' : 'Open tooltip'}
  </Button>
</div>

<div>Open: {open}</div>
