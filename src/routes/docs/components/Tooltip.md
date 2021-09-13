<script>
  import { mdiTrashCan } from '@mdi/js';

  import Button from '$lib/components/Button.svelte';
  import Grid from '$lib/components/Grid.svelte';
  import Preview from '$lib/components/Preview.svelte';
  import Tooltip from '$lib/components/Tooltip.svelte';
</script>

## Button

<Preview>
  <Tooltip title="Hello">
    <Button>Hover me</Button>
  </Tooltip>
</Preview>

## Icon button

<Preview>
  <Tooltip title="Click to remove">
    <Button icon={mdiTrashCan} class="w-12 h-12" />
  </Tooltip>
</Preview>

## Slot w/ custom markup

<Preview>
  <Tooltip>
    <Grid
          slot="title"
          templateColumns="auto 1fr"
          columnGap={16}
          rowGap={8}
          class="bg-gray-900/90 text-white px-4 py-2 text-xs rounded shadow"
        >
      <div class="col-span-2 justify-self-center text-sm">Tue, March 30</div>
      <div class="text-white/50 justify-self-end">Actual:</div>
      <div class="justify-self-end">123.50</div>
      <div class="text-white/50 justify-self-end">Target:</div>
      <div class="justify-self-end">90.00</div>
      <div class="text-white/50 justify-self-end">Variance:</div>
      <div class="justify-self-end">33.50</div>
    </Grid>
    <Button>Hover me</Button>
  </Tooltip>
</Preview>

## Placement

<Preview>
  <Tooltip title="Hello" placement="left">
    <Button>Left</Button>
  </Tooltip>
  <Tooltip title="Hello" placement="top">
    <Button>Top</Button>
  </Tooltip>
  <Tooltip title="Hello" placement="bottom">
    <Button>Bottom</Button>
  </Tooltip>
  <Tooltip title="Hello" placement="right">
    <Button>Right</Button>
  </Tooltip>
</Preview>

<!-- TODO: Slot with custom transition -->