<script>
	export let active = false;
</script>

<div class="laron-sidebar absolute w-screen h-screen bg-black bg-opacity-80 top-0" class:active>
	<div class="sidebar-content pt-20 h-screen overflow-auto md:w-1/3">sidebar</div>
</div>

<style>
	.laron-sidebar {
		transition: left 0.3s ease-in-out;
		left: -100%;
	}

	.laron-sidebar.active {
		left: 0;
	}
</style>
