<script lang="ts">
	import { page } from '$app/stores';

	const c = $page.url.searchParams.get('c');
	let e: string = '';
</script>

<div class="flex justify-center items-center h-screen">
	<form
		method="GET"
		action="https://l5amgfqtc7.execute-api.us-east-2.amazonaws.com/production/{c}?e={e}"
	>
		<div class="flex flex-col items-center space-y-3">
			<div>
				<input
					type="email"
					name="email"
					class="rounded-xl"
					placeholder="Type your email"
					bind:value={e}
				/>
			</div>
			<button
				type="submit"
				class="bg-blue-500 text-black p-2 px-3 rounded-xl hover:bg-blue-600 hover:text-white"
				>Submit</button
			>
		</div>
	</form>
</div>
