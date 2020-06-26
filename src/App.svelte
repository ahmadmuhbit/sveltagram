<script>
	import BigHeader from './components/BigHeader.svelte';
	import data from './instagram.json';
	import PhotoList from './components/PhotoList.svelte';

	export let hashtag;
</script>

<svelte:head>
	<link href="https://cdnjs.cloudflare.com/ajax/libs/bulma/0.8.0/css/bulma.min.css" rel="stylesheet" />
</svelte:head>

<main class="container">
	<BigHeader hashtag={hashtag} />
	<input type="text" bind:value={hashtag} />
	<pre>{data.graphql.hashtag.edge_hashtag_to_media.edges[0].node.accessibility_caption}</pre>
	<h1>Photos</h1>
	<PhotoList />
</main>
	
<style>
	h1 {
		color: #57A71C;
	}
</style>