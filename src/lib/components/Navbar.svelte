<!-- Script section to import assets and components -->
<script>
	import whiteWaves from '$lib/assets/whiteWaves.svg';  // Importing whiteWaves SVG
	import MobileNavbar from './MobileNavbar.svelte';    // Importing MobileNavbar Svelte component

	let mobileNavBar;  // Initializing variable to interact with MobileNavbar component
</script>

<!-- Container for navigation -->
<div class="nav-container">
	<!-- Navigation bar -->
	<nav class="nav">
		<!-- Logo with link to home -->
		<a href="/" class="logo-container">
			<img src="/favicon.png" alt="" class="logo" />
			<h1>Join <span>Artify</span></h1>
		</a>
		<!-- Navigation menu -->
		<ul class="nav-menu">
			<li class="nav-menu-items"><a href="/#about-us">About Us</a></li>
			<li class="nav-menu-items"><a href="/#benefits">Benefits</a></li>
			<li class="nav-menu-items"><a href="/#jobs">Jobs</a></li>
		</ul>
		<!-- Apply button linking to Google Forms -->
		<a
			href="https://docs.google.com/forms/d/e/1FAIpQLSewG6jXziVNkJgq_NvmdvO5BirikFQCoull85WH2_VK2Cec1g/viewform"
			target="_blank"
			rel="noopener noreferrer"
			id="apply"><button class="btn">Apply</button></a
		>
		<!-- Button to open mobile navigation -->
		<button class="bars" on:click={() => mobileNavBar.showModal()}>
			<svg
				xmlns="http://www.w3.org/2000/svg"
				fill="none"
				viewBox="0 0 24 24"
				stroke-width="2"
				stroke="currentColor"
				class="w-6 h-6"
			>
				<path
					stroke-linecap="round"
					stroke-linejoin="round"
					d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
				/>
			</svg>
		</button>
	</nav>
	<!-- White waves image at the bottom -->
	<img src={whiteWaves} alt="" class="wave" />
</div>

<!-- Including MobileNavbar component with binding to mobileNavBar -->
<MobileNavbar bind:dialog={mobileNavBar} />

<!-- Styling for navigation and container -->
<style>
	/* Styling for navigation container */
	.nav-container {
		position: fixed;
		width: 100%;
		z-index: 9999;
	}
	/* Styling for navigation bar */
	.nav {
		display: flex;
		justify-content: space-between;
		align-items: center;
		font-size: 1.2rem;
		padding: 12px 20%;
		background-color: white;
		box-sizing: border-box;
		font-weight: 500;
		user-select: none;
		text-align: center;
		height: 64px;
	}
	/* Styling for navigation menu items */
	.nav-menu-items {
		color: var(--violet);
		list-style: none;
		display: inline-block;
		padding: 0 20px;
	}
	/* Styling for logo container */
	.logo-container {
		display: flex;
		align-items: center;
		color: var(--grey);
		font-weight: 700;
		font-size: 1.5rem;
	}
	/* Styling for logo container on hover */
	.logo-container:hover {
		text-decoration: none;
	}
	/* Styling for span within logo container */
	.logo-container span {
		color: var(--red);
	}
	/* Styling for logo image */
	.logo {
		width: 50px;
		padding-right: 5px;
	}
	/* Styling for bars button (mobile navigation toggle) */
	.bars {
		width: 40px;
		background-color: rgba(255, 255, 255, 0);
		color: var(--grey);
		border: none;
		cursor: pointer;
		display: none;
	}
	/* Styling for white waves image */
	.wave {
		width: 100%;
		height: 20px;
	}

	/* Media queries for responsive design */
	@media (max-width: 1280px) {
		.nav {
			padding-left: 10%;
			padding-right: 10%;
		}
	}
	@media (max-width: 1024px) {
		.nav {
			padding-left: 5%;
			padding-right: 5%;
		}
	}
	@media (max-width: 768px) {
		.nav,
		#apply button {
			font-size: 1rem;
		}
		.logo-container {
			font-size: 1.3rem;
		}
		.logo {
			width: 40px;
		}
	}
	@media (max-width: 640px) {
		.nav-menu,
		#apply {
			display: none;
		}
		.bars {
			display: block;
		}
	}
</style>