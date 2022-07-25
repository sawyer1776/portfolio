<template>
	<section>
		<div>
			<ion-icon class="up" name="chevron-up"></ion-icon>
		</div>
		<ul>
			<a
				href="https://www.linkedin.com/in/clay-gibson-dev/"
				target="_blank"
				><ion-icon name="logo-linkedin"></ion-icon
			></a>

			<a
				href="https://github.com/sawyer1776"
				target="_blank"
				><ion-icon name="logo-github"></ion-icon
			></a>

			<a
				href="https://drive.google.com/file/d/1MnylCKoO67c7qAaA7sCearCyR-XUsX3-/view?usp=sharing"
				target="_blank"
				><ion-icon name="document-sharp"></ion-icon
			></a>
		</ul>
	</section>
</template>

<script>
export default {};
</script>

<style scoped>
section {
	background-color: var(--color-grey);
	color: white;
	padding: 7rem;
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
	gap: 2rem;
}
ul {
	display: flex;
	gap: 3rem;
	justify-content: center;
}

a {
	color: white;
	font-size: var(--font-s-7);
	transition: all 200ms;
}

a:hover,
a:active {
	transform: translateY(-0.5rem);
}

.up {
	font-size: var(--font-s-7);
}
</style>
