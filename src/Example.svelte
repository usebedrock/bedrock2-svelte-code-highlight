<script>
  import { onMount } from 'svelte'

  import Code from './Code.svelte'

  export let lang = 'xml'
  export let code
  export let horizontal = false

  let showCode = false

  function show() {
    showCode = true
  }

  function hide(e) {
    e.stopPropagation()
    showCode = false
  }
</script>

<style lang="scss">
  .snippet {
    position: relative;
    display: flex;
    justify-content: center;
    align-items: stretch;
    flex-direction: column;
  }

  .code {
    display: flex;
    flex-direction: column;
    align-items: stretch;
    overflow: hidden;
    position: relative;
  }

  :global(.codeview) {
    margin-bottom: 0 !important;
  }

  :global(.btn-show-code) {
    align-self: center;
    margin: 2em 0 0.5em;
    position: absolute;
    bottom: 0;
    background: none;
  }
</style>
<figure class="highlight">
    <div class="snippet" class:horizontal>
    <div class="preview">
        <slot name="preview" />
    </div>
    <div class="code">
        <Code {lang} {code} />
    </div>
    </div>
</figure>