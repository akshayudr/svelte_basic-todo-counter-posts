<script>
    export let year
	import { onMount } from 'svelte';

	let posts = [];
 
        onMount(async () => {
		const res = await fetch(`https://jsonplaceholder.typicode.com/users/1/posts`);
		posts = await res.json();
	});

	
</script>

<div>
<h1>Posts</h1>
{#each posts as post, index}
<h2>{index+1}-{post.title}</h2>
<p>{post.body}</p>
{/each}
</div>

<div>
    <p class="padding">©{year}</p>
</div>


<style>
    .padding {
        padding-left: 550px;
        padding-top: 10px;
    }
</style>