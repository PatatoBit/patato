<script lang="ts">
	import favicon from '$lib/assets/favicon.png';
	import '../styles/global.scss';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} type="image/png" />
	<link rel="apple-touch-icon" href="/apple-touch-icon.png" />

	<title>Chayapat Pakham</title>
	<meta
		name="description"
		content="Pat (Chayapat Pakham): web developer, artist and student from Thailand. Swift Student Challenge winner"
	/>

	<!-- Facebook Meta Tags -->
	<meta property="og:url" content="https://patato-beta.vercel.app/" />
	<meta property="og:type" content="website" />
	<meta property="og:title" content="Chayapat Pakham" />
	<meta
		property="og:description"
		content="Web developer, artist and student from Thailand. Swift Student Challenge winner"
	/>
	<meta property="og:image" content="https://patato-beta.vercel.app/og.jpg" />

	<!-- Twitter Meta Tags -->
	<meta name="twitter:card" content="summary_large_image" />
	<meta property="twitter:domain" content="patato-beta.vercel.app" />
	<meta property="twitter:url" content="https://patato-beta.vercel.app/" />
	<meta name="twitter:title" content="Chayapat Pakham" />
	<meta
		name="twitter:description"
		content="Web developer, artist and student from Thailand. Swift Student Challenge winner"
	/>
	<meta name="twitter:image" content="https://patato-beta.vercel.app/og.jpg" />
</svelte:head>

{@render children()}
