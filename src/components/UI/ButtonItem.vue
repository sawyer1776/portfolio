<template>
	<a :class="color ? 'alt' : 'primary'" :href="link">
		{{ title }}
	</a>
</template>

<script>
export default {
	props: ['title', 'color', 'link', 'small'],
};
</script>

<style scoped>
a {
	font-size: var(--font-s-6);

	padding: 1rem 3rem;

	transition: transform 200ms;
	text-decoration: none;
}
.primary {
	background-color: transparent;
	border: 0.25rem solid var(--color-primary);
	color: var(--color-primary);
}

.alt {
	background-color: var(--color-primary);
	border: 0.25rem solid var(--color-primary);
	color: white;
}

.small {
	font-size: var(--font-s-4);
	padding: 0.75rem 2rem;
}
.invert {
	color: white;
	padding: 0.5rem 1rem;
}

a:active,
a:hover {
	transform: translateY(-0.5rem);
	cursor: pointer;
}
</style>
