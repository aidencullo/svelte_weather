<script>
  let search = '';
  let countries = ['USA','Canada','France','Germany','Japan','Brazil'];
  $: filtered = countries.filter(c => c.toLowerCase().includes(search.toLowerCase()));
  let selected = '';
</script>

<input type="text" bind:value={search} placeholder="Search countries..."/>

<select bind:value={selected} size="5">
  {#each filtered as country}
    <option value={country}>{country}</option>
  {/each}
</select>

<p>Selected: {selected}</p>