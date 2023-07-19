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
				local: {
					id: 1,
					title: 'Local Farms Application',
					techs: [
						'React',
						'Asynchronous JavaScript',
						'Pocketbase',
						'CSS 3',
						'REST API',
						'Linux Servers',
					],
					paragraph:
						'Built to allow small farmers and backyard gardeners to quickly and easily list their produce for sale and allow buyers to connect with them to purchase locally grown produce. This applications features a simple in browser GUI that allows users to create and edit the database entries associated with their products and pages. Automatically generated custom web routes allow for an infinite number of products and producers that are all linkable. The code is modular highly reusable units that generate a page’s information from database API calls. React’s useContext() hook is used for sharing user authentication and basic user data throughout the application. Built with React.js, and Pocketbase. NOTE: Styling currently optimized for mobile first desktop styling still in progress',

					liveLink: 'http://137.184.98.71/all-sellers',
					codeLink:
						'https://github.com/sawyer1776/local-food-app',
					imgSrc: '../../img/local-farms.jpg',
				},
				whale: {
					id: 2,
					title: 'Website for Whale Animation',
					techs: ['JavaScript', 'HTML 5', 'CSS 3'],
					paragraph:
						'Commissioned to build the official website for the studio, Whale Animation.   Built with CSS, HTML, and JavaScript to be a simple and elegant site that showcases the studio’s work.  JavaScript is used to dynamically generate the HTML for the project pages from a JS object for easy updates and maintaince.',

					liveLink:
						'https://www.whaleanimationstudios.com/',
					codeLink:
						'https://github.com/sawyer1776/whale-animation',
					imgSrc: '../../img/whale-animation.png',
				},
				crypto: {
					id: 3,
					title: 'Crypto market tracker',
					techs: [
						'JavaScript',
						'HTML 5',
						'CSS 3',
						'Coinranking API',
					],
					paragraph:
						'Track and sort the changes in the crypto markets. Each column can be sorted by the data inside it. Selectable timeframes update the data to data from that period. Data is live from the Coinranking API.  Built with CSS, HTML, and JavaScript.',

					liveLink: 'https://cryptoataglance.netlify.app/',
					codeLink:
						'https://github.com/sawyer1776/cryptoataglance',
					imgSrc: '../../img/crypto-tracker.png',
				},

				cutlist: {
					id: 4,
					title: 'Cutlist Optimizer',
					techs: ['Vue', 'JavaScript', 'HTML 5', 'CSS 3'],
					paragraph:
						'Built to help carpenters quickly and easily list the cuts needed for each size of material and automatically calculate the total needed from each size of stock',

					liveLink:
						'https://cutlist-optimizer.netlify.app/',
					codeLink:
						'https://github.com/sawyer1776/cutlist-optimizer',
					imgSrc: '../../img/cutlist-optimizer.png',
				},
				// slider: {
				// 	id: 4,
				// 	title: 'Continuous Slider',
				// 	techs: ['JavaScript', 'HTML 5', 'CSS 3'],
				// 	paragraph:
				// 		'This app is built to run an infinite loop of images full screen.  Easily change the slide duration and transition time.  This was written for local use to run full screen ads.  Html is generated dynamically based on file names in the local folder.',
				// 	note: 'Note: Only built to run on Chrome, there will be errors on other browsers',
				// 	liveLink:
				// 		'https://physical-ad-slider.netlify.app/',
				// 	codeLink:
				// 		'https://github.com/sawyer1776/physical-ad-slider',
				// 	imgSrc: '../../img/cutlist-optimizer.png',
				// },
			},
		};
	},
};
</script>

<style scoped>
ul {
	display: flex;
	flex-direction: column;
	align-items: center;
}

h2 {
	margin-bottom: 4rem;
}
</style>
