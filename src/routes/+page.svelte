<script lang="ts">
	import { onMount } from 'svelte';
	import wa from '$lib/assets/images/wa.svg';
	import linkedin from '$lib/assets/images/linkedin.svg';
	import mailbox from '$lib/assets/images/mailbox.svg';

	let imgHidden: boolean = true;

	onMount(() => {
		imgHidden = false;
		console.log('death note is here')
	});
</script>

<div class="wrapper">
	<section id="about" class="hero">
		<aside class="hero-img">
			<div class="img" aria-hidden={imgHidden}>
			
			</div>
		</aside>
		<div class="bio">
			<h1>Hi, I'm Kevin!</h1>
			<p>I'm a Senior Software Engineer, with a sprinkle of UI/UX Design on top!</p>
			<p>
				I've always been passionate about this crazy place call the Internet, now I found a way to
				sit there for a living.
			</p>
			<p>Wanna know more? Head over to my <a href="#career">experiences...</a></p>
		</div>
	</section>
	<section id="career" class="career">
		<div class="career-content">
			<h1>Career and Experiences</h1>
			<ul>
				<li>
					<h2>NTT Data Italia</h2>
					<p>
						Lorem ipsum dolor sit amet consectetur adipisicing elit. Doloremque, laborum, doloribus,
						iste voluptatem quia delectus optio vel dignissimos aut minus nemo odio obcaecati
						aliquid nostrum quibusdam veniam sapiente ipsum asperiores.
					</p>
				</li>
				<li>
					<h2>Digitronica.it</h2>
					<p>
						Lorem, ipsum dolor sit amet consectetur adipisicing elit. Odit fugit numquam atque
						accusantium aperiam blanditiis explicabo, porro dolorem eaque corporis minus
						repellendus. Perspiciatis, omnis unde ab aut odio reiciendis voluptatem?
					</p>
				</li>
				<li>
					<h2>Università degli Studi di Verona</h2>
					<p>
						Lorem, ipsum dolor sit amet consectetur adipisicing elit. Odit fugit numquam atque
						accusantium aperiam blanditiis explicabo, porro dolorem eaque corporis minus
						repellendus. Perspiciatis, omnis unde ab aut odio reiciendis voluptatem?
					</p>
				</li>
			</ul>
		</div>
	</section>
	<section id="contacts" class="contacts">
		<h1>Wanna chat?</h1>
		<h2>Here are some places you can find me:</h2>
		<p>
			<img src={wa} alt="whatsapp" /> <span>+39 3407352713</span>
		</p>
		<p>
			<img src={linkedin} alt="linkedin" /> <a href="https://www.linkedin.com/in/kevin-mansoldo-2b99b3129/">My Linkedin Profile</a>
		</p>
		<p>
			<img src={mailbox} alt="mail" /> <span>kevin.mansoldo@gmail.com</span>
		</p>
	</section>
</div>

<style lang="scss">
	@use '../styles/shared';

	.wrapper {
		@include shared.main-subgrid();

		> * {
			padding: 2rem;
			min-height: 60vh;
			height: auto;
		}

		.hero {
			display: grid;
			grid-template-columns: repeat(2, 1fr);

			.hero-img {
				position: relative;

				.img {
					width: 40em;
					aspect-ratio: 1;
					background-color: red;
					position: absolute;
					left: -40em;
					opacity: 0;
				}

				// .img[aria-hidden='false'] {
					// transform: translateX(100%);
					// transition: transform ease-in 3s;
					// opacity: 1;
					// transition: opacity 0.8s;
				// }
			}

			.bio {
				margin: auto 0;
			}
		}

		.career {
			background-image: linear-gradient(
				transparent,
				var(--light-bg-lavender),
				var(--light-bg-lavender),
				transparent
			);
			background-position: 49px 100%;
			background-repeat: no-repeat;
			background-size: 2px 100%;

			> .career-content > h1 {
				padding: 2rem;
			}

			ul {
				display: flex;
				flex-direction: column;
				gap: 3rem;

				li {
					position: relative;
				}
			}

			ul li::marker {
				font-size: 2em;
			}
		}

		.contacts {
			p {
				padding-block: 2rem;
				display: flex;
				gap: var(--gap);
				align-items: center;

				span, a {
					font-size: var(--h3-fs);
					text-decoration: none;
					color: inherit;
				}
			}
		}
	}
</style>
