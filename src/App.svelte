<!-- Todo -->
<script>
	import Todo from "./Todo.svelte";
	import Counter from "./Counter.svelte";
	import Posts from "./Posts.svelte";
	const year = new Date().getFullYear()
</script>

<Todo />


<!-- Counter -->

<Counter name={10}/>



<!-- Posts -->

<Posts year={year}/>