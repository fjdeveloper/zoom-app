<script>
	import '../app.css';
</script>

<slot />

<style lang="postcss">
	:global(body) {
		background-image: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('/back.jpg');
		background-position: center center;
		background-repeat: no-repeat;
		background-size: cover;
	}
</style>
