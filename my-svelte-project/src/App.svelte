<script>
  let counter = $state(0)
  const increment = () => {
    counter += 1
  }
  const decrement = () => {
    counter -= 1
  }
</script>

<p>Counter: {counter}</p>

<button onclick={increment}>Increment</button>
<button onclick={decrement}>Decrement</button>