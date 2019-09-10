<script>
	import 'highlight.js/styles/github.css';
	import Example from './Example.svelte';
	import Button from './Button.svelte';
</script>

<Example
  code={`<Button>Weird flex but OK</Button>
<Button variant="primary">Weird flex but OK</Button>
<Button variant="success">Weird flex but OK</Button>`}>
  <div slot="preview">
	<Button>Weird flex but OK</Button>
	<Button variant="primary">Weird flex but OK</Button>
	<Button variant="success">Weird flex but OK</Button>
  </div>
</Example>