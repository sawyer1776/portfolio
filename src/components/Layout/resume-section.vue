<template>
	<section>
		<h2>About</h2>
		<p>
			I am a front end developer with a desire to solve real
			world problems with technology. I started out learning
			tech by deciding to get my
			<strong> Amazon Web Services</strong>
			Certified Solutions Architect certification. I hit the
			books and in less than three months was able to earn
			my certification with no prior experience. I have been
			learning new technologies ever since. I want to use my
			skills to make complicated technology easy to access
			for everyone.
		</p>

		<div>
			<button-item
				color="alt"
				title="Resume"
				target="_blank"
				href="https://drive.google.com/file/d/1UuaXKc_ZWA1oXCXKtIGCEqzZ5h9k7NM6/view?usp=sharing"
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
