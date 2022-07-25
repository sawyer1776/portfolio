<template>
	<section>
		<h2>Projects</h2>
		<ul>
			<project-item
				v-for="project in projects"
				:key="project.id"
				:title="project.title"
				:techs="project.techs"
				:paragraph="project.paragraph"
				:note="project.note"
				:liveLink="project.liveLink"
				:codeLink="project.codeLink"
				:imgSrc="project.imgSrc"
			></project-item>
		</ul>
		<div id="resume-section"></div>
	</section>
</template>

<script>
import ProjectItem from './ProjectItem.vue';

export default {
	components: { ProjectItem },
	data() {
		return {
			projects: {
				whale: {
					id: 1,
					title: 'Website for Whale Animation',
					techs: ['JavaScript', 'HTML 5', 'CSS 3'],
					paragraph:
						'The official website for the studio Whale Animation. Built from scratch by me without libraries of frameworks. Custorm script generates the slider content dynamically from an object.',
					note: 'Note: Mobile optimization coming soon, site is set to go live by the end of the month',
					liveLink: 'https://whale-animation.netlify.app/',
					codeLink:
						'https://github.com/sawyer1776/whale-animation',
					imgSrc: '../../img/whale-animation.png',
				},
				crypto: {
					id: 2,
					title: 'Crypto market tracker',
					techs: [
						'JavaScript',
						'HTML 5',
						'CSS 3',
						'Coinranking API',
					],
					paragraph:
						'Track and sort cypto the changes in the crypto markets.  Each column can be sorted by the data inside it.  Select the timeframe you want to sort from.  Data is live from the Coinranking API ',

					liveLink: 'https://cryptoataglance.netlify.app/',
					codeLink:
						'https://github.com/sawyer1776/cryptoataglance',
					imgSrc: '../../img/crypto-tracker.png',
				},

				cutlist: {
					id: 3,
					title: 'Cutlist Optimizer',
					techs: ['Vue', 'JavaScript', 'HTML 5', 'CSS 3'],
					paragraph:
						'Built to help carpenters quickly and easily list the cuts needed for each size of material and calculate the total needed from each size of stock',

					liveLink:
						'https://cutlist-optimizer.netlify.app/',
					codeLink:
						'https://github.com/sawyer1776/cutlist-optimizer',
					imgSrc: '../../img/cutlist-optimizer.png',
				},
				slider: {
					id: 4,
					title: 'Continuous Slider',
					techs: ['JavaScript', 'HTML 5', 'CSS 3'],
					paragraph:
						'This app is built to run an infinite loop of images full screen.  Easily change the slide duration and transition time.  This was written for local use to run full screen ads.  Html is generated dynamically based on file names in the local folder.',
					note: 'Note: Only built to run on Chrome, there will be errors on other browsers',
					liveLink:
						'https://physical-ad-slider.netlify.app/',
					codeLink:
						'https://github.com/sawyer1776/physical-ad-slider',
					imgSrc: '../../img/cutlist-optimizer.png',
				},
			},
		};
	},
};
</script>

<style scoped>
h2 {
	margin-bottom: 4rem;
}
</style>
