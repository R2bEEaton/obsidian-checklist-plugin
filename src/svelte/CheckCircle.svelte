<script lang="ts">
  export let checked = false
</script>

<div class="checkbox">
  <div class={(checked == 'x' || checked =='-') ? 'checked' : (checked == '/' ? 'inprog' : '')} />
</div>

<style>
  .checkbox {
    width: var(--checklist-checkboxSize);
    height: var(--checklist-checkboxSize);
    min-width: var(--checklist-checkboxSize);
    min-height: var(--checklist-checkboxSize);
    border-radius: 50%;
    border: var(--checklist-checkboxBorder);
    padding: 2px;
    position: relative;
  }

  .checked {
    background-color: var(--text-muted);
    width: var(--checklist-checkboxCheckedSize);
    height: var(--checklist-checkboxCheckedSize);
    border-radius: 50%;
    position: absolute;
    top: calc(calc(var(--checklist-checkboxSize) - var(--checklist-checkboxCheckedSize)) / 4);
    left: calc(calc(var(--checklist-checkboxSize) - var(--checklist-checkboxCheckedSize)) / 4);
  }

  .inprog {
      background-color: var(--text-muted);
      width: var(--checklist-checkboxCheckedSize);
      height: var(--checklist-checkboxCheckedSize);
      border-radius: 50%;
      background-color: #000;
        background-image: linear-gradient(to right, var(--text-muted) 50%, var(--background-secondary) 50%, var(--background-secondary) 100%);
        background-size: 100% 100%;
        background-repeat: no-repeat;
      position: absolute;
      top: calc(calc(var(--checklist-checkboxSize) - var(--checklist-checkboxCheckedSize)) / 4);
      left: calc(calc(var(--checklist-checkboxSize) - var(--checklist-checkboxCheckedSize)) / 4);
    }
</style>
