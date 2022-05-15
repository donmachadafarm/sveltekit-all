<script>
    // each demo and for deconstructing
	import Navbar from './../../components/Navbar.svelte';
	let cats = [
		{ id: 'J---aiyznGQ', name: 'Keyboard Cat' },
		{ id: 'z_AbfPXTKms', name: 'Maru' },
		{ id: 'OUtn3pvWmpg', name: 'Henri The Existential Cat' }
	];

    // each demo and for key-ing each blocks
    import Thing from './Thing.svelte';

	let things = [
		{ id: 1, name: 'apple' },
		{ id: 2, name: 'banana' },
		{ id: 3, name: 'carrot' },
		{ id: 4, name: 'doughnut' },
		{ id: 5, name: 'egg' },
	];

	function handleClick() {
		things = things.slice(1);
	}
</script>

<Navbar />

<div class="card w-96 bg-base-100 shadow-xl mt-4 ml-4">
    <div class="card-body">
      <h2 class="card-title">EACH DEMO(DECONSTRUCT) : The Famous Cats of YouTube</h2>
      <p>CATTSSSS</p>
        <ul>
        {#each cats as { id, name }, i}
            <li><a target="_blank" href="https://www.youtube.com/watch?v={id}">
                {i + 1}: {name}
            </a></li>
        {/each}
        </ul>
    </div>
</div>

<div class="card w-96 bg-neutral shadow-xl mt-4 ml-4">
    <div class="card-body">
        <h2 class="card-title">EACH DEMO(KEYS) : THINGS</h2>
        <p>THINGS</p>
        <button on:click={handleClick}>
            Remove first thing
        </button>
        
        {#each things as thing (thing.id) }
            <Thing name={thing.name}/>
        {/each}
    </div>
</div>