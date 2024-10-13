<script>
    export let index;
    export let todo;
    export let editTodo;
    export let removeTodo;

</script>

<div class="todo">
    <p>
        {index + 1}, {todo}
    </p>
    <div class="actions"> 
        <!-- svelte-ignore a11y-no-static-element-interactions -->
        <i 
            class="fa-regular fa-pen-to-square"
            on:click={() => { editTodo(index) }} 
            
            aria-label="Edit"
            on:keydown={() => {}}
        ></i>
        <!-- svelte-ignore a11y-no-static-element-interactions -->
        <i 
            class="fa-regular fa-trash-can"
            on:click={() => { removeTodo(index) }} 
            aria-label="Remove"
            on:keydown={() => {}}
        ></i>
    </div>
</div>

<style>
    .todo {
        border: left 1px solid cyan;
        padding: 8px 14px;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
    .actions {
        display: flex;
        align-items: center;
        gap: 14px;
        font-size: 1.3rem;
    }
    .actions i {
        cursor: pointer;
    }
    .actions i:hover {
        color: coral;
    }
</style>