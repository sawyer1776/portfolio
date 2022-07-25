<template>
	<li class="project">
		<div>
			<h3>{{ title }}</h3>
			<ul>
				<li
					class="tech"
					v-for="tech in techs"
					:key="tech.key"
				>
					<h4>{{ tech }}</h4>
				</li>
			</ul>

			<p class="paragraph">{{ paragraph }}</p>
			<p class="note">{{ note }}</p>
			<div class="buttons">
				<button-item
					class="small"
					color="alt"
					title="View site"
					target="_blank"
					v-bind:href="liveLink"
				/>
				<button-item
					class="small"
					title="View code"
					target="_blank"
					:href="codeLink"
				/>
			</div>
		</div>
		<div class="img-side">
			<img :src="imgSrc" />
			<!-- <p>subtext here</p> -->
		</div>
	</li>
</template>

<script>
import ButtonItem from '../UI/ButtonItem.vue';

export default {
	components: { ButtonItem },
	props: [
		'title',
		'techs',
		'paragraph',
		'note',
		'liveLink',
		'codeLink',
		'imgSrc',
	],
	methods: {
		getImage() {
			console.log(this.imgSrc);
			return require(this.imgSrc);
		},
	},
};
</script>

<style scoped>
.project {
	display: flex;
	gap: 4rem;
	margin: 0rem 4rem 8rem 4rem;
}
h3 {
	font-size: var(--font-s-5);
	margin-bottom: 2rem;
}

.paragraph {
	font-size: var(--font-s-3);
	margin-bottom: 2rem;
	max-width: 40vw;
	line-height: 1.5;
}
.note {
	margin-bottom: 3rem;
	font-size: var(--font-s-2);
	font-style: italic;
	color: #6a6a6a;
}

ul {
	display: flex;
	gap: 1rem;
	margin-bottom: 3rem;
}
.tech {
	font-size: var(--font-s-3);
	font-weight: 800;
	padding: 0.75rem 1rem;

	background-color: var(--color-primary-lightest);
	/* box-shadow: 0.2rem 0.2rem 0.5rem 0.2rem
		rgba(0, 0, 0, 0.05); */
}

.buttons {
	display: flex;
	gap: 2rem;
	margin-bottom: 4rem;
}

img {
	max-width: 50vw;
	box-shadow: 0.5rem 0.5rem 1.5rem 0.25rem
		rgba(0, 0, 0, 0.15);
}
</style>
