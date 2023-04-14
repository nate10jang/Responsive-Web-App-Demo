<script lang="ts">
	let sideNavVisible: boolean = false;

	function toggleSideNavbar() {
		sideNavVisible = !sideNavVisible;
	}
</script>

<header class="flex w-full bg-slate-800 fixed top-0 py-3 px-6 h-16">
	<nav class="flex flex-wrap justify-between items-center w-full">
		<a href="#" class="text-green-500 font-bold text-4xl">Brand</a>

		<ul class="list-none hidden sm:flex">
			<li>
				<a href="#" class="text-white p-3 font-medium text-xl">Home</a>
			</li>
			<li>
				<a href="#" class="text-white p-3 font-medium text-xl">About</a>
			</li>
			<li>
				<a href="#" class="text-white p-3 font-medium text-xl"
					>Services</a
				>
			</li>
			<li>
				<a href="#" class="text-white p-3 font-medium text-xl"
					>Contact</a
				>
			</li>
		</ul>

		<button
			class="text-white text-3xl sm:hidden"
			on:click={toggleSideNavbar}
		>
			&#9776;
		</button>
	</nav>
</header>

<div class="fixed top-0 right-0 h-screen w-60 bg-zinc-800 {sideNavVisible ? 'visible' : 'invisible'}">
	<button class="top-0 right-0 text-white text-4xl" on:click={toggleSideNavbar}>
		&times;
	</button>
</div>