<script lang="ts">
	import { browser } from '$app/environment';
	import { onMount } from 'svelte';

	export let useLabel = false;

	let fontSize = 0;

	onMount(() => {
		if (browser) {
			const container = document.querySelector<HTMLElement>('.logo-container');
			if (container !== null) {
				fontSize = (container.offsetWidth / 10) * 2;
			}
		}
	});

	$: imgWidth = useLabel ? '34%' : '100%';
</script>

<div class="logo-container flex items-center w-full">
	<div style="width: {imgWidth};">
		<svg
			version="1.1"
			xmlns="http://www.w3.org/2000/svg"
			xmlns:xlink="http://www.w3.org/1999/xlink"
			width="100%"
			height="100%"
			viewBox="-76,103,512,512"
			><g
				fill="none"
				fill-rule="nonzero"
				stroke="none"
				stroke-width="1"
				stroke-linecap="round"
				stroke-linejoin="round"
				stroke-miterlimit="10"
				stroke-dasharray=""
				stroke-dashoffset="0"
				font-family="none"
				font-weight="none"
				font-size="none"
				text-anchor="none"
				style="mix-blend-mode: normal"
				><g id="stage"
					><g id="layer1 1"
						><path d="M167.20232,377.24267" id="Path 1" fill="none" stroke="#000000" /><path
							d="M167.25808,377.28878"
							id="Path 1"
							fill="none"
							stroke="#000000"
						/><path d="M168.17108,384.60706" id="Path 1" fill="none" stroke="#000000" /><path
							d="M167.46451,376.72089"
							id="Path 1"
							fill="none"
							stroke="#000000"
						/><path
							d="M162.65748,324.34267l17.31556,8.51923l17.36948,-8.71272l-17.42543,34.85085zM189.50816,399.00265l2.99182,4.23108l-3.25818,4.60776l3.25818,4.60776l-2.99182,4.23108l2.99182,4.23107l-3.25817,4.60775l3.25818,4.60777l-12.5,17.67767l-12.5,-17.67767l3.25817,-4.60775l-3.25818,-4.60777l2.99182,-4.23107l-2.99182,-4.23108l3.25818,-4.60776l-3.25818,-4.60776l3.1806,-4.49804l-2.99182,-4.23107l3.0694,-4.34079l-3.25817,-4.60776l3.13899,-4.43921l-3.13898,-4.43919l2.80404,-3.96551l-2.80404,-3.96552l-91.83745,71.04759l-124.65835,32.5327l104.33745,-80.79424l112.15835,-29.27051v-6.52436l-112.15835,-29.27051l-104.33745,-80.79424l124.65835,32.5327l91.83745,71.1148v-8.23171l7.83342,15.72954l2.56592,5.15238l1.99413,4.00422l2.08706,-4.17411l2.32294,-4.64589l8.19653,-16.39307v8.55864l91.83745,-71.1148l124.65835,-32.5327l-104.33745,80.79424l-112.15835,29.27051v6.52436l112.15835,29.27051l104.33745,80.79424l-124.65835,-32.5327l-91.83745,-71.1148l-2.80404,4.03273l2.80404,3.96552l-3.13899,4.43921l3.13898,4.43919l-3.25818,4.60776l3.06939,4.34079l0.00002,-0.00003l0.18876,0.26695l-2.99171,4.23093z"
							id="CompoundPath 1"
							class="fill-blue-500"
							stroke-opacity="0"
							stroke="#000000"
						/></g
					></g
				></g
			></svg
		>
	</div>
	{#if useLabel}
		<span class="select-none text-blue-500" style="font-size: {fontSize}px;">LARON</span>
	{/if}
</div>
