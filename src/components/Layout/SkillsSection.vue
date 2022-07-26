<template>
	<section>
		<h2>Skills</h2>
		<ul>
			<li>
				<img
					src="../../../public/img/html.png"
					alt="HTML 5 logo"
				/>
				<h3>HTML 5</h3>
			</li>
			<li>
				<img
					src="../../../public/img/css.png"
					alt="CSS logo"
				/>
				<h3>CSS 3</h3>
			</li>
			<li>
				<img
					src="../../../public/img/java-script.png"
					alt="Java Script Logo"
				/>
				<h3>JavaScript</h3>
			</li>
			<li>
				<img
					src="../../../public/img/vue-js.png"
					alt="Vue.js Logo"
				/>
				<h3>Vue</h3>
			</li>
			<li>
				<img
					src="../../../public/img/aws.png"
					alt="AWS Logo"
				/>
				<h3>AWS</h3>
			</li>
			<li>
				<img
					src="../../../public/img/react.png"
					alt="react Logo"
				/>
				<h3>React</h3>
			</li>
			<li>
				<img
					src="../../../public/img/git-icon.png"
					alt="Git Logo"
				/>
				<h3>Git</h3>
			</li>
		</ul>
		<div id="projects-section"></div>
	</section>
</template>

<script>
export default {};
</script>

<style scoped>
section {
	background-color: var(--color-primary-lightest);

	border-top: 0.25rem solid var(--color-primary);
	border-bottom: 0.25rem solid var(--color-primary);
	box-shadow: 0.5rem 0.5rem 1.5rem 0.25rem
		rgba(0, 0, 0, 0.15);
	margin-bottom: 8rem;
}
ul {
	list-style: none;
	display: flex;
	justify-content: center;
	align-items: center;
	gap: 5rem;
	text-align: center;
}

h3 {
	padding-bottom: 1rem;
	font-size: var(--font-s-3);
	width: 8rem;
}

img {
	width: 8rem;
	height: 12rem;

	object-fit: contain;
	margin-bottom: 1rem;
}
/* 1000px */
@media (max-width: 62.5em) {
	img {
		width: 6rem;
		height: 9rem;
	}
	ul {
		gap: 3rem;
	}
}
@media (max-width: 53.125em) {
	ul {
		flex-wrap: wrap;
		margin-left: 14rem;
		margin-right: 14rem;
	}
}

@media (max-width: 48.875em) {
	ul {
		margin-left: 4rem;
		margin-right: 4rem;
	}
}
@media (max-width: 33.75em) {
	ul {
		margin-left: 1rem;
		margin-right: 1rem;
	}
}
</style>
