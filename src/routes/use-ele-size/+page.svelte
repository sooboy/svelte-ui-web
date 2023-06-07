
<script>
	import { useElementSize } from '@svelteuidev/composables';

	const [elementSize, ref] = useElementSize();

	$: ({ width, height } = $elementSize);
</script>

<textarea use:ref style='width: 400px; height: 120;' />
<div>Width: {width}px, height: {height}px</div>