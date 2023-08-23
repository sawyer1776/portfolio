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
						'Built to allow small farmers and backyard gardeners to quickly and easily list their produce for sale and allow buyers to connect with them to purchase locally grown produce. This applications features a simple in browser GUI that allows users to create and edit the database entries associated with their products and pages. Automatically generated custom web routes allow for an infinite number of products and producers that are all linkable. The code is modular highly reusable units that generate a page’s information from database API calls. React’s useContext() hook is used for sharing user authentication and basic user data throughout the application. Built with React.js, and Pocketbase.',

					liveLink: 'http://137.184.98.71/all-sellers',
					codeLink:
						'https://github.com/sawyer1776/local-food-app',
					imgSrc: '../../img/local-farms.jpg',
				},
				fire: {
					id: 2,
					title: 'Find Fire Digital',
					techs: ['Nuxt.js', 'Vue.js', 'CSS 3'],
					paragraph:
						'Built as a brand site for Find Fire Digital.  Using nuxt static site generations for SEO and performance. Features contact form with realtime data validation. Seamless page transitions with Nuxt transitions. Script to show phone and email dynamically by generating it in JavaScript to avoid spam bots.  ',

					liveLink: 'https://findfiredigital.com/',
					codeLink:
						'https://github.com/sawyer1776/find-fire',
					imgSrc: '../../img/find-fire.jpg',
				},
				whale: {
					id: 3,
					title: 'Whale Animation Studios',
					techs: ['JavaScript', 'HTML 5', 'CSS 3'],
					paragraph:
						'Commissioned to build the official website for the studio, Whale Animation.   Built with CSS, HTML, and JavaScript to be a simple and elegant site that showcases the studio’s work.  JavaScript is used to dynamically generate the HTML for the project pages from a JS object for easy updates and maintaince.',

					liveLink:
						'https://www.whaleanimationstudios.com/',
					codeLink:
						'https://github.com/sawyer1776/whale-animation',
					imgSrc: '../../img/whale-animation.png',
				},
				trout: {
					id: 4,
					title: 'Black Trout Woodworking',
					techs: ['Nuxt.js', 'Vue.js', 'CSS 3'],
					paragraph:
						'Marketing site for Black Trout Woodworking.  Built with Nuxt.js for SEO and performance.  Features a contact form with realtime data validation. Gallery component. ',

					liveLink: 'https://blacktroutwoodworking.com/',
					codeLink:
						'https://github.com/sawyer1776/black-trout-woodworking',
					imgSrc: '../../img/black-trout.jpg',
				},
				crypto: {
					id: 5,
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
