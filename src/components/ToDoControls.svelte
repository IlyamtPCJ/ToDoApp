<script>
    import { createEventDispatcher } from "svelte";
    const dispatch = createEventDispatcher();
    
    let inputValue = '';
    function onClick() {
        if(inputValue.length) {
            dispatch('add', {text: inputValue});
            inputValue = '';
        }
    }
</script>

<div class="todo-controls">
    <input class="todo-controls_input" type="text" bind:value={inputValue} />
    <button class="todo-controls_btn" on:click={onClick}>Add</button>
</div>

<style>
    .todo-controls {
        display: grid;
        grid-template-columns: 70% 30%;
    }

    .todo-controls_input {
        border: none;
        border-radius: 10px 0 0 10px;
        padding: 15px;
    }

    .todo-controls_btn {
        border: none;
        border-radius: 0 10px 10px 0;
        background: rgb(237, 214, 12);
    }
</style>
