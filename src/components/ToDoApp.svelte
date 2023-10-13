<script>
	import ToDoControls from "./ToDoControls.svelte";
	import ToDoItem from "./ToDoItem.svelte";

    const items = [
        {
            id: 1,
            text: 'Some Todo',
            isDone: false,
        },
        {
            id: 2,
            text: 'Some Todo 2',
            isDone: false,
        },
    ]
</script>
<div class="todo-app">
    <ToDoControls />
    <div class="todo-app_field">
        {#each items as item}
            <ToDoItem id={item.id} text={item.text} isDone={item.isDone}/>
        {/each}
    </div>
</div>

<style>
    .todo-app {
        width: 700px;
        height: 80%;
        background: rgb(196, 193, 193);
        border-radius: 15px;
        padding: 40px;
        display: flex;
        flex-direction: column;
        gap: 30px;
    }
    .todo-app_field {
        background: white;
        flex-grow: 1;
        border-radius: 15px;
        overflow-y: auto;
        padding: 15px;
        display: flex;
        flex-direction: column;
        gap: 20px;
    }
</style>