<template>
	<section>
		<h2>About Me</h2>
		<p>
			I am a front end developer with a desire to solve real
			world problems with technology. A US army veteran, I
			started out learning tech by deciding to get my
			<strong> Amazon Web Services</strong> certified
			solutions architect certification. I hit the books and
			in less than three months was able to earn my
			certification with no prior experience. I have been
			learning new technologies ever since. I want to use my
			skills to make complicated technology easy to access
			for everyone.
		</p>

		<div>
			<button-item
				color="alt"
				title="Resume"
				target="_blank"
				href="https://drive.google.com/file/d/1MnylCKoO67c7qAaA7sCearCyR-XUsX3-/view?usp=sharing"
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
</style>
