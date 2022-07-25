<template>
	<section id="hero-section">
		<div>
			<h1>Hi, I'm <span>Clay Gibson</span></h1>
			<h2>A Front End Developer</h2>

			<ul>
				<button-item
					color="alt"
					title="Skills"
					href="#skills-section"
				></button-item>

				<button-item
					title="Projects"
					href="#projects-section"
				></button-item>

				<button-item
					title="About"
					href="#resume-section"
				></button-item>

				<button-item
					title="Contact"
					href="#contact-section"
				></button-item>
			</ul>
			<div id="skills-section"></div>
		</div>
	</section>
</template>

<script>
import ButtonItem from '../UI/ButtonItem.vue';

export default {
	components: { ButtonItem },
	props: ['name', 'listType', 'cutlist'],
	emits: ['new-cutlist-item'],
	data() {
		return {
			enteredValueQty: null,
			enteredValueLength: null,
		};
	},
	methods: {},
};
</script>

<style scoped>
section {
	height: 100vh;
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
}

h1 {
	font-size: var(--font-s-10);
	margin-bottom: 2rem;
}

h1 span {
	color: var(--color-primary);
}

h2 {
	font-size: var(--font-s-7);
	align-self: flex-start;
	text-align: start;
	font-weight: 400;
	margin-bottom: 4rem;
}

ul {
	list-style: none;
	display: flex;
	gap: 2rem;
}
</style>
