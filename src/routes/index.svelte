<script>
	import axios from 'axios'

	let res = ''
	let input

	const get = async () => {
		console.log(input)
		const {data} = await axios.get(input)
		res = data
	}
</script>

<style>
.button {
	height: 40px;
	width: 100px;
	background-color: goldenrod;
	cursor: pointer;
}

</style>


<input bind:value={input} />
<div class="button" on:click={get}>
	Get
</div>
response: {JSON.stringify(res)}
