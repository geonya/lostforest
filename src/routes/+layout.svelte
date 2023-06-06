<script lang="ts">
	import '../global.css';
</script>

<header>
	<nav>
		<a href="/">Logo</a>
		<a href="/about">Menu</a>
		<a href="/about">Reservation</a>
		<a href="/about">Contact</a>
	</nav>
</header>
<slot />

<style>
	header {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 3rem;
		z-index: 2;
	}
	nav {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 0 1rem;
	}
</style>
