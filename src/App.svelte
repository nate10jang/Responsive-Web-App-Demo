<script>
	import Content from "./lib/Content.svelte";
	import NavigationBar from "./lib/NavigationBar.svelte";
	import Sidebar from "./lib/Sidebar.svelte";
</script>

<NavigationBar />
<div class="flex flex-wrap">
	<Sidebar />
	<Content />
</div>
