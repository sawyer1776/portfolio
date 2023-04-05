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
				title="About"
				href="#resume-section"
				class="small invert"
			></button-item>

			<button-item
				title="Contact"
				href="#contact-section"
				class="small invert"
			></button-item>
			<a
				target="_blank"
				href="https://drive.google.com/file/d/1a8XMZm_Y-MhSHMLQLeZLpTP1altqbqIO/view?usp=sharing"
			>
				<ion-icon name="document-sharp"></ion-icon>
			</a>
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
	z-index: 999;
}
ul {
	list-style: none;
	display: flex;
	gap: 3rem;
}

a {
	color: white;
	font-size: var(--font-s-6);
	transition: all 200ms;
}

a:hover,
a:active {
	transform: translateY(-0.5rem);
}
/* 750px */
@media (max-width: 50em) {
	nav {
		display: none;
	}
}
</style>
