<script lang="ts">
	let thing: string = 'something';
    let stuff: string[] = []
</script>

<!-- <svelte:head>
    <script 
        defer 
        async 
        src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&callback=initMap"
    />
</svelte:head> -->

<div>
	<div>{thing}</div>
	<button class="btn bg-primary text-primary-content" on:click={() => {thing = `${thing}+1`; stuff.push('a ha'); stuff = stuff}}>
		click me
	</button>
    <ul>
        {#each stuff as thing, idx}
            <li>{thing}</li>
            <a class="btn btn-secondary" href={`map/${idx}`}>user {idx}</a>
        {/each}
    </ul>
</div>
