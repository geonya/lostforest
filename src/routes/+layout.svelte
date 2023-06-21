<script lang="ts">
	import '../global.css';
</script>

<header>
	<nav>
		<a id="Logo" href="/">Logo</a>
		<div class="nav-content">
			<a href="/?section=About">About</a>
			<a href="/?section=Food">Food</a>
			<a href="/?section=Reservation">Reservation</a>
			<a href="/store">Store</a>
		</div>
		<a href="/contact">Contact</a>
	</nav>
</header>
<slot />

<style>
	header {
		position: fixed;
		top: 0;
		left: 0;
		width: 100%;
		height: 3rem;
		z-index: 10;
	}
	nav {
		display: flex;
		height: 100%;
		justify-content: space-between;
		align-items: center;
		padding: 0 1rem;
	}
	#Logo {
		font-size: 1.1rem;
		font-weight: bold;
	}
	nav a {
		font-size: 0.9rem;
	}
	.nav-content {
		display: flex;
	}

	.nav-content a {
		margin-right: 1rem;
	}
	.nav-content a:last-child {
		margin-right: 0;
	}
</style>
