<script lang="ts">
</script>

<hero>
	<section class="hero_content">
		<div />
		<div style="line-height: 0.3rem;">
			<h1>Lost Forest</h1>
			<h4>Only the lost find a new way</h4>
		</div>
		<h3>2023.07 Coming Soon</h3>
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
		height: 100%;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		align-items: center;
		text-align: center;
	}
	.hero_content h1 {
		font-size: 6rem;
		letter-spacing: 2rem;
	}
	.hero_content h4 {
		font-size: 2rem;
		letter-spacing: 0.9rem;
	}
	.hero_content h3 {
		font-size: 2rem;
		letter-spacing: 0.6rem;
		margin-bottom: 8rem;
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
