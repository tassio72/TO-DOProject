<template>
	<div id="app">
		<h1>Tarefas</h1>
		<new-task @taskAdded='addTask'/>
		<task-grid :tasks="tasks" 
		@taskDeleted="deleteTask()"/>
	</div>
	

</template>

<script>
import NewTask from './componentes/NewTask'
import TaskGrid from './componentes/TaskGrid'

export default {
	components: { 'task-grid': TaskGrid, 'new-task': NewTask},
	data () {
		return {
			tasks: []
		}
	},
	methods: {
		addTask(task) {
			if(task.name) {

				const sameName = t => t.name === task.name //função guardada dentro de sameName para ser usada em filter
				const reallyNew = this.tasks.filter(sameName).length == 0;
	
				if(reallyNew) {
					this.tasks.push({
						name: task.name,
						pending: true //ele colocou named.pending || true
					})
				}

			}
		},
		deleteTask(index) {
			this.tasks.splice(index, 1)

		}
	}


}
</script>

<style>
	body {
		font-family: 'Lato', sans-serif;
		background: linear-gradient(to right, rgb(22, 34, 42), rgb(58, 96, 115));
		color: #FFF;
	}

	#app {
		display: flex;
		flex: 1;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		height: 100vh;
	}

	#app h1 {
		margin-bottom: 5px;
		font-weight: 300;
		font-size: 3rem;
	}
</style>
