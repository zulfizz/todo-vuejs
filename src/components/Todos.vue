<template>
	<div class="container-fluid">
		<ul class="list-group">
		<li class="list-group-item" v-bind:key="todo.id" v-for="todo in todos">
			<TodoItem v-bind:todo="todo" v-on:del-todo="$emit('del-todo', todo.id)" />
		</li>
		</ul>
	</div>
</template>

<script>
	import TodoItem from './TodoItem.vue';

	export default{
		name: "Todos",
		components: {
			TodoItem
		},
		props: ['todos']
	}
</script>