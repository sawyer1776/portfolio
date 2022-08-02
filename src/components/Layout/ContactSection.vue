<template>
	<section>
		<h2>Contact</h2>
		<form
			name="contact"
			method="post"
			action="https://clay-gibson-dev.com/#projects-section"
			data-netlify="true"
			data-netlify-honeypot="bot-field"
			netlify
		>
			<input
				type="hidden"
				name="form-name"
				value="contact"
			/>

			<input
				type="name"
				placeholder="Name"
				name="name"
				id="name"
				required
			/>
			<input
				type="email"
				placeholder="Email"
				name="email"
				id="email"
				required
			/>
			<input
				name="message"
				class="message"
				type="text"
				placeholder="Message"
				id="message"
				required
			/>
			<button type="submit">Submit</button>
		</form>
	</section>
</template>

<script>
export default {};
</script>

<style scoped>
form {
	display: flex;
	flex-direction: column;

	margin: 0 auto;
	gap: 1rem;
	max-width: 60rem;
}

input {
	padding: 0.75rem 1rem;
}

.message {
	height: 15rem;
	padding: 1rem 1rem 13rem 0.75rem;
}
button {
	max-width: fit-content;
	align-self: center;
	margin-top: 1rem;
	padding: 1rem 3rem;

	font-size: var(--font-s-7);

	padding: 1rem 3rem;

	transition: all 200ms;
	text-decoration: none;

	background-color: var(--color-primary);
	border: none;
	color: var(--wht);
}

button:hover {
	transform: scale(1.05);
	cursor: pointer;
}

button:active {
	transform: translateX(0.5rem);
}
@media (max-width: 50em) {
	button {
		font-size: var(--font-s-5);
	}
}
</style>
