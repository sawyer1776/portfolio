<template>
	<li class="project">
		<div class="text-side">
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
			<!-- <div @click="playYt()" class="background">
				<ion-icon name="logo-youtube"></ion-icon>
			</div> -->

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
		playYt(id) {
			console.log(id);
		},
	},
};
</script>

<style scoped>
.project {
	display: flex;
	gap: 4rem;
	margin: 0rem 4rem 8rem 4rem;
	width: fit-content;
}
h3 {
	font-size: var(--font-s-5);
	margin-bottom: 2rem;
}

.paragraph {
	font-size: var(--font-s-3);
	margin-bottom: 2rem;
	/* max-width: 40vw; */
	width: 40vw;
	max-width: 65rem;
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
	width: 50vw;
	max-width: 170rem;
	box-shadow: 0.5rem 0.5rem 1.5rem 0.25rem
		rgba(0, 0, 0, 0.15);
}
.img-side {
	position: relative;
	height: fit-content;
}

.background {
	width: 100%;
	height: 100%;
	top: 0;
	left: 0;
	position: absolute;
	background-color: rgba(0, 0, 0, 0.25);

	justify-content: center;
	align-items: center;
	display: flex;
	opacity: 0%;
	transition: opacity 250ms;
}

ion-icon {
	font-size: var(--font-s-9);
	color: white;
}
.background:hover,
.background:active {
	cursor: pointer;
	opacity: 100%;
}

.visible {
	opacity: 100%;
}
/* 1200px */
@media (max-width: 75em) {
	ul {
		flex-wrap: wrap;
	}
}
/* 850px */
@media (max-width: 53.125em) {
	.project {
		flex-direction: column;
		justify-content: center;
		align-items: center;
		max-width: 90vw;
	}
	img {
		width: 100%;
		max-width: 100%;
		box-shadow: 0.5rem 0.5rem 1.5rem 0.25rem
			rgba(0, 0, 0, 0.15);
	}
	.text-side {
		max-width: 90vw;
	}
	.paragraph {
		font-size: var(--font-s-4);

		width: 100%;
	}

	.note {
		font-size: var(--font-s-3);
	}

	.img-side {
		order: -1;
	}
	.project {
		gap: 3rem;
		margin: 0rem 0rem 4rem 0rem;
	}
}
</style>
