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
					class="hero"
				></button-item>

				<button-item
					title="Projects"
					href="#projects-section"
					class="hero"
				></button-item>

				<button-item
					title="About"
					href="#resume-section"
					class="hero"
				></button-item>

				<button-item
					title="Contact"
					href="#contact-section"
					class="hero"
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
	width: 100vw;
	height: 100vh;
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
}

h1 {
	font-size: var(--font-s-11);
	margin-bottom: 2rem;
}

h1 span {
	color: var(--color-primary);
}

h2 {
	font-size: var(--font-s-8);
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

/* 1200px */
@media (max-width: 75em) {
	h1 {
		font-size: var(--font-s-10);
		margin-bottom: 2rem;
	}

	h2 {
		font-size: var(--font-s-7);
	}
}
/* 750px */
@media (max-width: 50em) {
	h1 {
		font-size: var(--font-s-8);
		margin-bottom: 2rem;
		line-height: 1.2;
	}

	h2 {
		font-size: var(--font-s-5);
	}
	ul {
		gap: 1.25rem;
	}
}
/* 500px*/
@media (max-width: 31.26em) {
	ul {
		flex-wrap: wrap;
	}
}
/* 428px */
@media (max-width: 26.75em) {
	span::before {
		content: '\A';
		white-space: pre;
	}
}
</style>
