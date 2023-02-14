<script lang="ts">
	import { page } from '$app/stores';

	export let c = $page.url.searchParams.get('c');
	let email: string = '';
</script>

<div class="flex justify-center items-center h-screen">
	<form
		method="GET"
		action="https://l5amgfqtc7.execute-api.us-east-2.amazonaws.com/production/{c}?e={email}"
	>
		<div class="flex flex-col items-center space-y-3">
			<div>
				<label for="email" class="font-bold">Email:</label>
				<input
					type="email"
					name="email"
					class="rounded-xl"
					placeholder="type your email"
					bind:value={email}
				/>
			</div>
			<button type="submit" class="bg-blue-500 text-white p-2 px-3 rounded-xl hover:bg-blue-600"
				>Submit</button
			>
		</div>
	</form>
</div>
