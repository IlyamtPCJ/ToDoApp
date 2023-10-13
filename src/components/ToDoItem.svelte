<script>
    // export let id;
    export let text;
    // export let isDone;
</script>


<div class="todo-item">
    <input class="todo-item_check" type="checkbox" />
    <span class="todo-item_text">{text}</span>
    <button class="todo-item_btn">Del</button>
</div>

<style>
    .todo-item {
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 15px;
        background: rgb(235, 100, 100);
        border-radius: 15px;
    }

    .todo-item_check {

    }
    .todo-item_text {
        flex-grow: 1;
    }
    .todo-item_btn {
        border: none;
        border-radius: 10px;
        background-color: chocolate;
        padding: 10px;
        min-width: 100px;
    }
</style>