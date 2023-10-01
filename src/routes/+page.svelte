<h1> To do list </h1>

<h2>IEEE</h2>

<style>
    h1 {color:red;}
    h2 {color: blue;}
  </style>

<script>
    let todos = [];
    function addTodo() {
        todos = [...todos,''];
    }
    function removeSelf(indeX) {
        todos = [...todos.slice(0, indeX), ...todos.slice(index+1)];
    }
</script>
{#each todos as todo, index}
<input bind:value={todos[index]}>
<button on:click={()=>removeSelf(index)}>X</button>
<br />

{/each}
<button on:click={addTodo}>Add</button>