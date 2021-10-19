<script lang="ts">
  import { Router, Route } from "svelte-navigator";
	import Home from "./pages/home/Home.svelte";
	import Levels from "./pages/levels/Levels.svelte";
</script>

<Router>
	<main>
		<Route path="/">
			<Home />
		</Route>

		<Route path="/levels">
			<Levels />
		</Route>
	</main>
</Router>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>