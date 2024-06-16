<!-- Script to export dialog for interaction -->
<script>
	export let dialog;
</script>

<!-- Dialog element for mobile navigation -->
<dialog bind:this={dialog}>
	<!-- Container for mobile navigation -->
	<div class="mobile-nav-container">
		<nav>
			<!-- Button to close dialog -->
			<button class="close" on:click={() => dialog.close()}>
				<svg
					xmlns="http://www.w3.org/2000/svg"
					fill="none"
					viewBox="0 0 24 24"
					stroke-width="2"
					stroke="currentColor"
					class="w-6 h-6"
				>
					<path stroke-linecap="round" stroke-linejoin="round" d="M6 18 18 6M6 6l12 12" />
				</svg>
			</button>
			<!-- Mobile navigation menu -->
			<ul class="mobile-nav-menu">
				<!-- Logo with link to home -->
				<a href="/" class="logo" on:click={() => dialog.close()}>
					<img src="/favicon.png" alt="" />
					<h1>Join <span>Artify</span></h1>
				</a>
				<!-- Menu items -->
				<li class="mobile-nav-menu-items">
					<a href="/#about-us" on:click={() => dialog.close()}>About Us</a>
				</li>
				<li class="mobile-nav-menu-items">
					<a href="/#benefits" on:click={() => dialog.close()}>Benefits</a>
				</li>
				<li class="mobile-nav-menu-items">
					<a href="/#jobs" on:click={() => dialog.close()}>Jobs</a>
				</li>
				<!-- Apply button linking to Google Forms -->
				<a
					href="https://docs.google.com/forms/d/e/1FAIpQLSewG6jXziVNkJgq_NvmdvO5BirikFQCoull85WH2_VK2Cec1g/viewform"
					target="_blank"
					rel="noopener noreferrer"
					id="apply"><button class="btn" on:click={() => dialog.close()}>Apply</button></a
				>
			</ul>
		</nav>
	</div>
</dialog>

<!-- Styling for the dialog and mobile navigation -->
<style>
	/* Dialog styling */
	dialog {
		width: 50%;
		height: 40%;
		border: none;
		margin: auto;
		border-radius: 40px;
		user-select: none;
	}
	/* Backdrop styling for dialog */
	dialog::backdrop {
		backdrop-filter: blur(5px);
	}
	/* Container styling for mobile navigation */
	.mobile-nav-container {
		z-index: 999;
		width: 100%;
		height: 100%;
		font-size: 1.2rem;
		font-weight: 500;
		display: flex;
		justify-content: center;
		align-items: center;
	}
	/* Styling for mobile navigation menu */
	.mobile-nav-menu {
		list-style: none;
		padding: 0;
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 1.2rem;
		color: var(--violet);
	}
	/* Close button styling */
	.close {
		width: 35px;
		background-color: rgba(255, 255, 255, 0);
		color: var(--grey);
		border: none;
		cursor: pointer;
		position: absolute;
		top: 20px;
		right: 20px;
	}
	/* Logo styling */
	.logo {
		display: flex;
		align-items: center;
		color: var(--grey);
		font-weight: 700;
		font-size: 1.5rem;
	}
	/* Logo hover styling */
	.logo:hover {
		text-decoration: none;
	}
	/* Visited link styling for logo */
	.logo:visited {
		color: var(--grey);
	}
	/* Styling for span within logo */
	.logo span {
		color: var(--red);
	}
	/* Styling for logo image */
	img {
		width: 50px;
		padding-right: 5px;
	}
</style>