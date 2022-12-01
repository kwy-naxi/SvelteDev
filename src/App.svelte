<script>
  import { onMount } from "svelte";

  let todos = [
    {
      id: 1,
      title: "스터디",
      completed: false,
    },
  ];

  let inputValue = "";

  function addTodo() {
    todos = [
      { id: todos.length, title: inputValue, completed: false },
      ...todos,
    ];
  }

  function setDone(todoId) {
    todos = todos.map((todo) => {
      if (todo.id === todoId) todo.completed = true;
      return todo;
    });
  }

  onMount(async () => {
    const res = await fetch("https://jsonplaceholder.typicode.com/todos");
    todos = await res.json();
  });
</script>

<main>
  <h1>Todo Application</h1>

  <div class="container">
    <input bind:value={inputValue} placeholder="What do you wanna do?" />
    <button on:click={addTodo}> Add</button>
    <ul>
      {#each todos as todo}
        <li class:done={todo.completed}>
          {todo.title} <button on:click={setDone(todo.id)}>Finish</button>
        </li>
      {/each}
    </ul>
  </div>
</main>

<style>
  h1 {
    margin-top: 4rem;
  }

  main {
    font-family: sans-serif;
    text-align: center;
    width: 40rem;
    margin: 0 auto;
  }

  .container {
    margin: 0px auto;
    text-align: center;
  }

  ul {
    padding: 0 6rem;
    font-size: 0.9rem;
  }

  li > button {
    margin-left: 1rem;
    font-size: 0.9rem;
  }

  input {
    width: 25rem;
    padding: 0.4rem;
    margin-bottom: 1rem;
  }

  button {
    height: 2rem;
  }

  .done {
    text-decoration: line-through;
  }
</style>
