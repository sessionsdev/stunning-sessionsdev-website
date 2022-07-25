<script>
	import Router from "./Router.svelte";
	import Route from "./Route.svelte";

	// pages
	import HomePage from "./page/HomePage.svelte";
	import ClientsPage from "./page/ClientsPage.svelte";
	import MyWorkPage from "./page/MyWorkPage.svelte";
	import TestingPage from "./page/TestingPage.svelte";
	import HireMePage from "./page/HireMePage.svelte";
</script>

<!-- <ul>
	<li><a href="/">Home</a></li>
	<li><a href="/main">Main</a></li>
	<li><a href="/about">About</a></li>
</ul> -->

<Router hashbang={false}>
	<Route path="/"><HomePage /></Route>
	<Route path="/my-clients"><ClientsPage /></Route>
	<Route path="/my-work"><MyWorkPage /></Route>
	<Route path="/hire-me"><HireMePage /></Route>
	<Route path="/testing"><TestingPage /></Route>
</Router>

<style lang="scss" global>
	@import 'src/styles/global.scss';
</style>