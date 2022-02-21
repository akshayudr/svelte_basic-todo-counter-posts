<!-- Todo -->

<script>
   let todos = [];
   let newItem= '';
   function handleAdd(){
       todos = [newItem, ...todos];
       newItem= '';
   }

   function deleteItem(value) {
        todos=todos.filter((i) => i !== value);
        
   }
</script>


<h1>Todo</h1>
<input bind:value={newItem} placeholder="new item">
<button class="btn-add" on:click={handleAdd}>Add</button>
{#each todos as todo }
<li>{todo}</li>
<button class="btn" on:click={() => deleteItem(todo)}>x</button>   
{/each}
{#if todos.length < 1}
	<p>Empty List</p>
{/if}

<hr style="height:2px;border-width:0;color:gray;background-color:gray">

<style>
.btn {
  display: inline-block;
  background: #000;
  color: #fff;
  border: none;
  padding: 5px 1a0px;
  margin: 1px;
  border-radius: 5px;
  cursor: pointer;
  text-decoration: none;
  font-size: 10px;
  font-family: inherit;
}


.btn-add {
  display: inline-block;
  background: #000;
  color: #fff;
  border: none;
  padding: 10px 20px;
  margin: 5px;
  border-radius: 5px;
  cursor: pointer;
  text-decoration: none;
  font-size: 15px;
  font-family: inherit;
}
</style>






