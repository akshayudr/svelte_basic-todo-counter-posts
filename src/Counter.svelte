<script>
  let value = 0;

  function handleIncrement() {
      value = value+1;
  }

  function handleDecrement() {
      value = value-1;
  }
</script>



<h1>Count: {value}</h1>
<button class="btn" on:click={handleIncrement}>+</button>
<button class="btn" on:click={handleDecrement}>-</button>

<hr style="height:2px;border-width:0;color:gray;background-color:gray">




<style>
    .btn {
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