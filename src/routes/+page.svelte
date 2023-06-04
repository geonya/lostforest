<hero>
	<section class="hero_content">
		<h1>Welcome to Lost Forest</h1>
		<h3>Only the lost find a new way.</h3>
	</section>
</hero>

<video src="/videos/bg-forest.mp4" autoplay muted loop />

<style>
	hero {
		position: fixed;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		display: grid;
		place-items: center;
		z-index: 1;
	}
	.hero_content {
		display: grid;
		place-items: center;
		text-align: center;
		color: #fff;
	}
	.hero_content h1 {
		font-size: 3rem;
	}
	.hero_content h3 {
		font-size: 1.5rem;
	}
	video {
		position: fixed;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		object-fit: cover;
		z-index: -1;
	}
</style>
