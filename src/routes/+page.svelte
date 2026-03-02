<script lang="ts">
	import readme from '/README.md?raw';
	import { marked } from 'marked';
	import classmates from '$lib/assets/mpc.jpeg';

	let about = marked.parse(readme);
	const h1 = '<h1>MPC Class Chatbot</h1>';
	about = about.toString().replace(h1, '');
</script>

<svelte:head>
	<title>MPC Class Chatbot</title>
	<script
		data-id="9265874266"
		id="chatling-embed-script"
		type="text/javascript"
		src="https://chatling.ai/js/embed.js"
	></script>
</svelte:head>

<main
	class="mx-auto prose px-4 py-5 prose-neutral
  lg:prose-lg prose-headings:my-3 prose-headings:text-primary/85
  prose-h1:mt-0 prose-h1:mb-5 prose-h1:text-center prose-h1:text-primary prose-li:my-0"
>
	{@html h1}
	<img src={classmates} alt="Happy students!" class="rounded-md shadow-lg shadow-primary" />
	{@html about}
</main>
