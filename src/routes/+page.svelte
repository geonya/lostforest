<script lang="ts">
	import { page } from '$app/stores';
	import { env } from '$env/dynamic/public';
	import { afterUpdate, tick } from 'svelte';

	let main: HTMLElement;

	const fetchInstagram = async () => {
		const requestData = {
			client_id: '1358203908061719',
			client_secret: env.PUBLIC_INSTAGRAM_API_KEY,
			code: 'AQCASiIHm5zFG5dZOxliZmekiVJj0MVmHpQwhTNhWoJTfmvC2rz19LRXItMmZRhgtxNSF_ZdSLyXqJK_HN-S5fmM03UHjKuSjvE1vIvLy050XdIli4jOXRrvKVbJY7o4CKOQRHcIlySiJxDarEsV3H9aCjYpC54P3-S_MfwrRol6fDqvdA3TKcmK4UUAUXy8NzWHY4AVwDEQBSw5iaYaZHDk2gjS_HLYMX4Htj-5i-wywQ',
			grant_type: 'authorization_code',
			redirect_uri: 'https://lostforest.co.kr/'
		};
		try {
			const response = await fetch('https://api.instagram.com/oauth/access_token', {
				method: 'POST',
				headers: {
					'Content-Type': 'application/json'
				},
				body: JSON.stringify(requestData)
			});
			if (response.ok) {
				const data = await response.json();
				console.log(data);
			} else {
				console.error(response);
			}
		} catch (error) {
			console.error(error);
		}
	};

	afterUpdate(() => {
		const queryParams = $page.url.searchParams.get('section');
		if (queryParams) {
			tick().then(() => {
				const section = document.getElementById(queryParams);
				if (section) {
					section.scrollIntoView({ behavior: 'smooth' });
				}
			});
		} else {
			main.scrollTo({ top: 0, behavior: 'smooth' });
		}
	});
</script>

<main bind:this={main}>
	<article id="Main">
		<video src="/videos/bg-forest.mp4" autoplay muted loop playsinline />
		<section class="section_content">
			<div />
			<div>
				<button on:click={fetchInstagram}>Instagram</button>
				<h1>LOST FOREST</h1>
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
	<article id="Food">
		<section class="section_content">
			<div />
			<div>
				<h2>Food</h2>
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
		overflow-x: hidden;
		scroll-snap-type: y mandatory;
		-webkit-overflow-scrolling: touch;
		height: 100vh;
	}
	article {
		scroll-snap-align: start;
		/* only supported in Chrome */
		scroll-snap-stop: always;
		width: 100%;
		height: 100%;
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
		pointer-events: none;
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
