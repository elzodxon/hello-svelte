<div>
	<h1>Welcome to SvelteKit</h1>
	<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

	<input bind:value="{todo}" type="text" placeholder="new todo item.."/>

	<button on:click="{ addTodo }">Add todo</button>
	<br>
	<ul>
		{#each todoList as item}
			<li>{item.text}</li>
		{/each}
	</ul>
</div>


<script>


let todo = 'hi'
let todoList = [{text: 'Write my first post', status: true},
	{text: 'Upload the post to the blog', status: false},
	{text: 'Publish the post at Facebook', status: false}];

const addTodo = ()=> {
	todoList = [...todoList, {text: todo, status: false}];
	// todoList.push({text: todo, status: false});
	todo = '';
}


</script>


<style>
.title {
	color: blue;
}
</style>