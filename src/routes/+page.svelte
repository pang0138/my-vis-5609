<script>
  let maxClick = 2; // default value
  let cnt = 0;

  function onClick() {
    if (cnt < maxClick) {
      cnt += 1;
    } else {
      alert("No more clicks allowed!");
    }
  }
</script>

<h1>[Mingyang]'s VIS Site</h1>
<img width="200" src="/image/gopher.jpg" alt="Gopher" />

<div>
  You can click up to
  <select bind:value={maxClick}>
    {#each [1, 2, 3, 4, 5, 6] as optionNum}
      <option value={optionNum}>{optionNum}</option>
    {/each}
  </select>
  times.
</div>

<button on:click={onClick}>Click me</button>
<p>Current clicks: {cnt}</p>
