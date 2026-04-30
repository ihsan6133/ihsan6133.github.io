<script lang="ts">
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
	<link rel="preconnect" href="https://fonts.googleapis.com">
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin="">
	<link href="https://fonts.googleapis.com/css2?family=Inter:ital,opsz,wght@0,14..32,100..900;1,14..32,100..900&display=swap" rel="stylesheet">

</svelte:head>

{@render children()}

<style>
	:global(body) {
		font-family: 'Inter', sans-serif;
		background-color: var(--background);
		line-height: 1.5;
		margin: 0;
	}

	
	:global(::selection) {
		background-color: var(--selection);
		color: var(--primary);
	}
	
	:global(::-webkit-scrollbar) {
		width: 8px;
		height: 8px;
	}
	
	:global(::-webkit-scrollbar-track) {
		background: transparent;
	}
	
	:global(::-webkit-scrollbar-thumb) {
		background-color: var(--primary-light);
		border-radius: 4px;
		
	}

	:global(:root) {
		--primary: rgb(30, 30, 30, 0.9);
		--primary-dark: rgb(0, 0, 0);
		--primary-light: rgba(0, 0, 0, 0.6);

		--background: rgb(244, 244, 244);
 
		--accent: #009678;
		--accent-light: rgb(25 167 138 / 45%);
		
		--selection: rgba(0, 150, 120, 0.2);
	}

	:global(:root[data-theme='dark']) {
		--primary: rgba(229, 229, 229, 0.9);
		--primary-dark: rgba(255, 255, 255, 0.8);
		--primary-light: rgba(255, 255, 255, 0.6);

		--background: rgb(15, 15, 15);

		--accent: #3ab59c;
		--accent-light: rgb(47 212 179 / 60%);

		--selection: rgba(65, 254, 216, 0.2);

	}
	
	@media (prefers-color-scheme: dark) {
		:global(:root:not([data-theme='light'])) {
			--primary: rgba(229, 229, 229, 0.9);
			--primary-dark: rgba(255, 255, 255, 0.8);
			--primary-light: rgba(255, 255, 255, 0.6);

			--background: rgb(15, 15, 15);

			--accent: #3ab59c;
			--accent-light: rgb(47 212 179 / 60%);

			--selection: rgba(65, 254, 216, 0.2);
		}
	}

</style>