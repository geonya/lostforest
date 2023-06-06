<script lang="ts">
</script>

<main>
	<article id="Main">
		<video src="/videos/bg-forest.mp4" autoplay muted loop playsinline />
		<section class="section_content">
			<div />
			<div>
				<h1>Lost Forest</h1>
				<h4>Only the lost find a new way</h4>
			</div>
			<h3>2023.07 Coming Soon</h3>
		</section>
	</article>
	<article id="About" style="background-color:#444;">
		<section class="section_content">
			<div />
			<div>
				<h2>Only the lost find a new way</h2>
				<h4>잃어버린 사람만이 새로운 길을 찾는다.</h4>
			</div>
			<h3>나만의 숲속 작은 산장, Lost Forest</h3>
		</section>
	</article>
	<article id="Menu">
		<section class="section_content">
			<div />
			<div>
				<h2>Menu</h2>
				<h4>맛있는 커피, 베이커리, 브런치가 있는 곳</h4>
			</div>
			<h3>나만의 숲속 작은 산장, Lost Forest</h3>
		</section>
	</article>
	<article id="Reservation" style="background-color:#444;">
		<section class="section_content">
			<div />
			<div>
				<h2>Reservation</h2>
				<h4>우리만의 공간 Lost Foreset</h4>
			</div>
			<h3>나만의 숲속 작은 산장, Lost Forest</h3>
		</section>
	</article>
	<article id="Contact">
		<section class="section_content">
			<div />
			<div>
				<h2>Contact</h2>
				<h4>010-2382-8410</h4>
				<h4>lostforestcafe@naver.com</h4>
			</div>
			<h3>나만의 숲속 작은 산장, Lost Forest</h3>
		</section>
	</article>
</main>

<style>
	main {
		overflow-y: scroll;
		scroll-snap-type: y mandatory;
		-webkit-overflow-scrolling: touch;
		height: 100vh;
	}
	article {
		scroll-snap-align: start;
		/* only supported in Chrome */
		scroll-snap-stop: always;
		width: 100%;
		height: 100vh;
		position: relative;
		display: grid;
		place-items: center;
		background-color: #333;
	}
	section {
		height: 100%;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		align-items: center;
		text-align: center;
		z-index: 2;
	}
	video {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: auto;
		object-fit: cover;
		z-index: 1;
	}
	@media (min-aspect-ratio: 16/9) {
		video {
			width: 100%;
			height: auto;
		}
	}
	@media (max-aspect-ratio: 16/9) {
		video {
			width: auto;
			height: 100%;
		}
	}
	@media (max-width: 375px) {
		section h1 {
			font-size: 1rem;
			letter-spacing: 0.5rem;
		}
		section h2 {
			font-size: 1.5rem;
			letter-spacing: 0.6rem;
		}
		section h4 {
			font-size: 0.5rem;
			letter-spacing: 0.2rem;
		}
		section h3 {
			font-size: 0.7rem;
			letter-spacing: 0.3rem;
			margin-bottom: 4rem;
		}
	}
	@media (min-width: 375px) {
		section h1 {
			font-size: 2rem;
			letter-spacing: 0.5rem;
		}
		section h2 {
			font-size: 1.5rem;
			letter-spacing: 0.4rem;
		}
		section h4 {
			font-size: 0.8rem;
			letter-spacing: 0.2rem;
		}
		section h3 {
			font-size: 0.8rem;
			letter-spacing: 0.3rem;
			margin-bottom: 4rem;
		}
	}
	@media (min-width: 768px) {
		section h1 {
			font-size: 3rem;
			letter-spacing: 0.5rem;
		}
		section h2 {
			font-size: 2rem;
			letter-spacing: 0.4rem;
		}
		section h4 {
			font-size: 1rem;
			letter-spacing: 0.2rem;
		}
		section h3 {
			font-size: 1.2rem;
			letter-spacing: 0.7rem;
			margin-bottom: 4rem;
		}
	}
	@media (min-width: 1200px) {
		section h1 {
			font-size: 4rem;
			letter-spacing: 1.5rem;
		}
		section h2 {
			font-size: 3rem;
			letter-spacing: 1rem;
		}
		section h4 {
			font-size: 1rem;
			letter-spacing: 0.6rem;
		}
		section h3 {
			font-size: 1.2rem;
			letter-spacing: 0.3rem;
			margin-bottom: 4rem;
		}
	}
</style>
