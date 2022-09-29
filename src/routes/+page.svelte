<script>
	import axios from 'axios';

	import { onMount } from 'svelte';

	let docList = [];

	onMount(async () => {


  
	});

    async function handleSubmit(){


        try {
            const res = await axios.get(`https://earsip-sveltekit-e5qk1zuoe-mashanz.vercel.app/api/klasifikasi`);
            console.log(res.data);
        } catch (e) {
			console.log(e)
            
        }
	
		

    }
</script>

<div class="container mx-auto">
	<div class="flex flex-col">
		<div>Enter Search</div>
		<div class="bg-green-600 border-dashed ">
			<form on:submit|preventDefault={handleSubmit}>
				<input type="text" class="form-input w-full" />
			</form>
		</div>
		<div>02</div>
		<div>03</div>
	</div>
</div>
