<script>
  let count = 0

  const increaseCount = () => {
    count+=1
  }

  const resetCount = () => {
    count=0
  }
</script>

<div class="hero min-h-screen bg-base-200">
    <div class="hero-content flex-col lg:flex-row-reverse">
      <img alt='monke' src="images/1.png" class="max-w-sm rounded-lg shadow-2xl" />
      <div>
        <h1 class="text-5xl font-bold">Current value on the counter is {count}</h1>
        <p class="py-6">Add 1 to each press of a button!</p>
        <button on:click={increaseCount} class="btn btn-primary">Button clicked {count} {count == 1 ? 'time' : 'times'}</button>
        <button on:click={resetCount} class="btn btn-secondary">Reset</button>
      </div>
    </div>
</div>