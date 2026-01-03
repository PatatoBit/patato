<script lang="ts">
	import favicon from '$lib/assets/favicon.svg';
	import '../styles/global.scss';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />

	<title>Pat's corner of the internet</title>
	<meta name="description" content="" />

	<!-- Facebook Meta Tags -->
	<meta property="og:url" content="https://patato-beta.vercel.app/" />
	<meta property="og:type" content="website" />
	<meta property="og:title" content="Pat's corner of the internet" />
	<meta property="og:description" content="" />
	<meta property="og:image" content="YOUR_IMAGE_URL_HERE" />

	<!-- Twitter Meta Tags -->
	<meta name="twitter:card" content="summary_large_image" />
	<meta property="twitter:domain" content="patato-beta.vercel.app" />
	<meta property="twitter:url" content="https://patato-beta.vercel.app/" />
	<meta name="twitter:title" content="Pat's corner of the internet" />
	<meta name="twitter:description" content="" />
	<meta name="twitter:image" content="YOUR_IMAGE_URL_HERE" />
</svelte:head>

{@render children()}
