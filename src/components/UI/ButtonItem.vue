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
	font-size: var(--font-s-7);

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
	font-size: var(--font-s-5);
	padding: 0.75rem 2rem;
}
.invert {
	color: white;
	padding: 0.5rem 1rem;
}

a:hover {
	transform: scale(1.05);
	cursor: pointer;
}

a:active {
	transform: translateX(0.5rem);
}
/* 1200px */
@media (max-width: 75em) {
	a {
		font-size: var(--font-s-6);
	}
	.small {
		font-size: var(--font-s-4);
	}
}
/* 750px */
@media (max-width: 50em) {
	a {
		font-size: var(--font-s-5);
	}
	.small {
		font-size: var(--font-s-4);
	}
	.hero {
		font-size: var(--font-s-4);
		padding: 0.5rem 1.5rem;
	}
}
@media (max-width: 18.75em) {
	a {
		font-size: var(--font-s-4);
		padding: 0.75rem 2rem;
	}
	.small {
		font-size: var(--font-s-3);
		padding: 0.5rem 1rem;
	}
}
</style>
