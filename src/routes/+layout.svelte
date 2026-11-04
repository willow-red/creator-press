<script lang="ts">
	import Header from './Header.svelte';
	import Footer from './Footer.svelte';
	import './layout.css';
	import favicon from '#lib/assets/favicon.svg';
	import type { LayoutProps } from './$types';
	let { children }: LayoutProps = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>
	<Header />
	<main>
		{@render children()}
	</main>
	<Footer />
