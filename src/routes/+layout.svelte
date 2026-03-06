<script lang="ts">
	import '@fontsource-variable/tiktok-sans';
	import './layout.css';
	import { page } from '$app/state';

	let { children } = $props();
	const { origin, hostname } = page.url;
	const title = 'MPC Class chatbot';
	const desc = `The MPC Class Chatbot is a conversational AI assistant designed to provide information about the MPC class, including fun stories and anecdotes about the class and its teachers.`;
	const mpcImage = origin + '/mpc.jpeg';
</script>

<svelte:head>
	<!-- Open Graph Meta Tags -->
	<meta property="og:url" content={origin} />
	<meta property="og:type" content="website" />
	<meta property="og:title" content={title} />
	<meta property="og:description" content={desc} />
	<meta property="og:image" content={mpcImage} />

	<!-- Twitter Meta Tags -->
	<meta name="twitter:card" content="summary_large_image" />
	<meta property="twitter:domain" content={hostname} />
	<meta property="twitter:url" content={origin} />
	<meta name="twitter:title" content={title} />
	<meta name="twitter:description" content={desc} />
	<meta name="twitter:image" content={mpcImage} />
</svelte:head>

{@render children()}
