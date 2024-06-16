<!-- Import necessary assets -->
<script>
	import blueWaves from '$lib/assets/blueWaves.svg';
</script>

<!-- Jobs section -->
<section id="jobs">
	<!-- Container for job cards -->
	<div class="cards-container">
		<!-- Job card for Website Builder Head -->
		<div class="card">
			<h1>Website Builder Head</h1>
			<ul class="card-list">
				<li>Create the general idea for the website and work with a group to accomplish it</li>
				<li>Develop leadership abilities</li>
			</ul>
		</div>
		<!-- Job card for Website Builder / Designer -->
		<div class="card">
			<h1>Website Builder / Designer</h1>
			<ul class="card-list">
				<li>Work with a team to update and design the website</li>
				<li>Develop your website design skills</li>
			</ul>
		</div>
	</div>
	<!-- Container for more job cards -->
	<div class="cards-container">
		<!-- Job card for Graphic Designer -->
		<div class="card">
			<h2 class="asterisk">*</h2>
			<h1 class="special-h1">Graphic Designer</h1>
			<ul class="card-list">
				<li>Work as a team with PR & Digital Marketing to make drawings for posts or stickers.</li>
				<li>Draw Colby!</li>
			</ul>
		</div>
		<!-- Job card for PR Member -->
		<div class="card">
			<h2 class="asterisk">*</h2>
			<h1 class="special-h1">PR Member</h1>
			<ul class="card-list">
				<li>Post on different social media accounts</li>
				<li>Coordinate with Graphic Designers and Digital Marketing</li>
			</ul>
		</div>
		<!-- Job card for Project Designer -->
		<div class="card">
			<h2 class="asterisk">*</h2>
			<h1 class="special-h1">Project Designer</h1>
			<ul class="card-list">
				<li>Come up with your project</li>
				<li>Launch the project with Artify</li>
				<li>Gain leadership experience</li>
			</ul>
		</div>
	</div>
	<!-- Note about commitment level -->
	<p>* These require less commitment</p>
	<!-- Apply button linking to Google Forms -->
	<a
		href="https://docs.google.com/forms/d/e/1FAIpQLSewG6jXziVNkJgq_NvmdvO5BirikFQCoull85WH2_VK2Cec1g/viewform"
		target="_blank"
		rel="noopener noreferrer"
		id="apply"><button class="btn">Apply</button></a>
</section>

<!-- Styling for the jobs section and its elements -->
<style>
	/* Jobs section styling */
	#jobs {
		background-color: var(--violet);
		height: 100%;
		display: flex;
		flex-direction: column;
		gap: 2rem;
		justify-content: center;
		align-items: center;
		padding: 60px 0;
	}
	/* Cards container styling */
	.cards-container {
		display: flex;
		flex-direction: row;
		gap: 2rem;
		justify-content: center;
		flex-wrap: wrap;
	}
	/* Card styling */
	.card {
		background-color: white;
		width: 300px;
		height: 400px;
		border-radius: 40px;
		transition: 0.2s;
		line-height: 1.5rem;
	}
	/* Card hover effect */
	.card:hover {
		transform: translateY(-5px);
	}
	/* Asterisk styling */
	.asterisk {
		color: var(--red-dark);
		margin: 10px 0 0 20px;
		font-size: 2rem;
		user-select: none;
	}
	/* Card header styling */
	.card h1 {
		text-align: center;
		font-weight: 700;
		font-size: 1.8rem;
		color: var(--red);
		user-select: none;
		padding: 0 25px;
		margin: 80px 0 50px 0;
		line-height: 1.8rem;
	}
	/* Special header styling */
	.special-h1 {
		margin-top: 30px !important;
	}
	/* List styling inside card */
	.card-list {
		list-style: disc;
		color: var(--violet);
		font-size: 1.2rem;
		padding: 0 50px;
	}
	/* List item styling */
	.card-list li {
		margin: 10px 0;
	}
	/* Paragraph styling */
	p {
		text-align: center;
		color: var(--red-dark);
		background-color: white;
		width: 300px;
		font-weight: 500;
		border-radius: 40px;
		padding: 15px 0 15px 0;
	}
</style>