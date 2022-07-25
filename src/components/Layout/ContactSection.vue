<template>
	<section>
		<h2>Contact</h2>
		<form
			name="contact"
			method="post"
			action=""
			data-netlify="true"
			data-netlify-honeypot="bot-field"
			netlify
		>
			<input
				type="hidden"
				name="form-name"
				value="contact"
			/>
			<input type="name" placeholder="Name" id="Name" />
			<input type="email" placeholder="Email" id="Email" />
			<input
				id="message"
				class="message"
				type="text"
				placeholder="Message"
			/>
			<button type="submit">send</button>
			<button-item
				type="submit"
				class="button"
				color="alt"
				title="Submit"
			/>
		</form>
	</section>
</template>

<script>
import ButtonItem from '../UI/ButtonItem.vue';
export default {
	components: { ButtonItem },
};
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
.button {
	max-width: fit-content;
	align-self: center;
	margin-top: 1rem;
}
</style>
