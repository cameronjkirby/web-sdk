<script lang="ts">
	import { Rectangle, Sprite } from 'pixi-svelte';
	import { getContext } from '../game/context';

	const context = getContext();
	const sizes = $derived(context.stateLayoutDerived.canvasSizes());
</script>

<Rectangle 
	{...sizes} 
	backgroundColor={0x1a0a2e} 
	zIndex={-3} 
/>

<Sprite
	key="mm_bg"
	width={sizes.width}
	height={sizes.height}
	anchor={{ x: 0, y: 0 }}
	x={0}
	y={0}
	zIndex={-2}
/>