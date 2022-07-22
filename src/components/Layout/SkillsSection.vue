<template>
	<section id="skills-section">
		<h2>My Skills</h2>
		<ul>
			<li>
				<img src="../../img/html.png" alt="HTML 5 logo" />
				<h3>HTML 5</h3>
			</li>
			<li>
				<img src="../../img/css.png" alt="CSS logo" />
				<h3>CSS 3</h3>
			</li>
			<li>
				<img
					src="../../img/java-script.png"
					alt="Java Script Logo"
				/>
				<h3>JavaScript</h3>
			</li>
			<li>
				<img src="../../img/vue-js.png" alt="Vue.js Logo" />
				<h3>Vue</h3>
			</li>
			<li>
				<img src="../../img/aws.png" alt="AWS Logo" />
				<h3>AWS</h3>
			</li>
			<li>
				<img src="../../img/react.png" alt="react Logo" />
				<h3>React</h3>
			</li>
			<li>
				<img src="../../img/git-icon.png" alt="Git Logo" />
				<h3>Git</h3>
			</li>
		</ul>
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
</style>
