<header>
	<div class="header-content">
		<div class="logo">KM</div>
		<nav>
			<ul>
				<li><a href="#about">About Me</a></li>
				<li><a href="#career">Career</a></li>
				<li><a href="#contacts">Contacts</a></li>
			</ul>
		</nav>
	</div>
</header>

<style lang="scss">
	@use '../styles/shared' as shared;

	header {
		@include shared.main-subgrid();

		.header-content {
			background: hsla(0, 0%, 100%, 0.3);
			backdrop-filter: blur(2em);
			color: var(--light-bg-lavender);
			border-radius: var(--border-radius);
			padding: var(--padding) 2rem;
			margin-top: 1rem;
			display: flex;
			justify-content: space-between;
			align-items: center;

			nav {
				ul {
					list-style: none;
					display: flex;
					gap: var(--gap);

					li a {
						background-image: linear-gradient(var(--light-bg-lavender), var(--light-bg-lavender));
						background-position: 0 100%;
						background-repeat: no-repeat;
						background-size: 0 2px;
						color: rgb(var(--light-bg-lavender) / 1);
						text-decoration: none !important;
						transition:
							background-size 0.3s,
							color 0.3s;
					}

					li a:hover {
						background-size: 100% 2px;
						color: rgb(var(--light-bg-lavender) / 1);
					}
				}
			}
		}
	}
</style>
