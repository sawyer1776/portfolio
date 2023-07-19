<template>
	<section>
		<h2>About</h2>
		<p>
			I am a front end developer with a desire to solve real
			world problems with technology. I started out learning
			tech by deciding to get my
			<strong> Amazon Web Services</strong>
			Certified Solutions Architect certification. I was
			quickly able to earn this certification through
			focused self study. Since then I have been focused on
			learning Front end skills focusing first on
			JavaScript, HTML and CSS before diving into the world
			of React. I want to use my skills to make complicated
			technology easy to access for everyone.
		</p>

		<div>
			<button-item
				color="alt"
				title="Resume"
				target="_blank"
				href="https://drive.google.com/file/d/1OgXrpzoUIMpJ9tyxxtl0_gzelHitd1b9/view?usp=sharing"
			></button-item>
			<button-item
				title="Contact"
				href="#contact-section"
			></button-item>
		</div>
		<div id="contact-section"></div>
	</section>
</template>

<script>
import ButtonItem from '../UI/ButtonItem.vue';
export default {
	components: { ButtonItem },
};
</script>

<style scoped>
section {
	display: flex;
	flex-direction: column;
	gap: 2rem;
	background-color: var(--color-primary-lightest);

	align-items: center;
}
div {
	display: flex;
	gap: 2rem;
}
p {
	max-width: 80rem;
	line-height: 1.5;
	font-size: var(--font-s-4);
}
/* 850px */
@media (max-width: 53.125em) {
	section {
		max-width: 100vw;
	}
	p {
		max-width: 60rem;
		line-height: 1.5;
		font-size: var(--font-s-4);
		padding: 1rem;
	}
}

@media (max-width: 18.75em) {
	p {
		line-height: 1.5;
		font-size: var(--font-s-3);
		padding: 0.25rem;
	}
}
</style>
