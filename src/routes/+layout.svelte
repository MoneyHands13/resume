<script lang="ts">
	import Header from '../components/Header.svelte';
	import Footer from '../components/Footer.svelte';
	import '../style.css';
</script>

<main>
	<Header />
	<slot />
	<Footer />
</main>

<style lang="scss" global>
    @use '../styles/shared' as shared;

	main {
		@include shared.main-grid();
	}
</style>
