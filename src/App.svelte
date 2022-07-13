<script>
  import Nested from "./Nested.svelte";

  const pkg = {
    name: 'svelte',
    version: 3,
    speed: 'быстро',
    website: 'https://svelte.dev'
  }
</script>

<Nested name={pkg.name} version={pkg.version} speed={pkg.speed} website={pkg.website}/>
<Nested {...pkg}/>