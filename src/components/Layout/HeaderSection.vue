<template>
	<nav>
		<ul>
			<button-item
				color="alt"
				title="Skills"
				href="#skills-section"
				class="small invert"
			/>

			<button-item
				title="Projects"
				href="#projects-section"
				class="small invert"
			></button-item>

			<button-item
				title="Resume"
				href="#resume-section"
				class="small invert"
			></button-item>

			<button-item
				title="Contact"
				href="#contact-section"
				class="small invert"
			></button-item>
		</ul>
	</nav>
</template>

<script>
import ButtonItem from '../UI/ButtonItem.vue';
export default {
	components: { ButtonItem },
};
</script>

<style scoped>
nav {
	padding: 1rem 4rem;
	width: 100vw;
	position: fixed;
	display: flex;
	justify-content: flex-end;
	background-color: var(--color-primary);
}
ul {
	list-style: none;
	display: flex;
	gap: 3rem;
}
</style>
