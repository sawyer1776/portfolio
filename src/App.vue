<template>
	<header-section></header-section>
	<hero-section></hero-section>
	<skills-section></skills-section>
	<projects-section></projects-section>
	<resume-section></resume-section>
	<contact-section></contact-section>
	<footer-section></footer-section>
</template>

<script>
import ContactSection from './components/Layout/ContactSection.vue';
import HeaderSection from './components/Layout/HeaderSection.vue';
import HeroSection from './components/Layout/HeroSection.vue';
import ProjectsSection from './components/Layout/ProjectsSection.vue';
import ResumeSection from './components/Layout/resume-section.vue';
import SkillsSection from './components/Layout/SkillsSection.vue';
import FooterSection from './components/Layout/FooterSection.vue';

export default {
	components: {
		HeroSection,
		HeaderSection,
		SkillsSection,
		ProjectsSection,
		ResumeSection,
		ContactSection,
		FooterSection,
	},
	name: 'App',
	methods: {},
};
</script>

<style>
* {
	padding: 0;
	margin: 0;
	box-sizing: border-box;
}

html {
	font-size: 62.5%;
	scroll-behavior: smooth;
}

body {
	overflow-x: hidden;
	font-family: 'Roboto Slab', sans-serif;
	line-height: 1;
	font-weight: 400;
	color: var(--color-grey);

	/* position: relative; */
}

section {
	padding: 4rem;
	justify-content: center;
}

h2 {
	font-size: var(--font-s-7);
	margin-bottom: 3rem;
	text-align: center;
}

ul {
	list-style: none;
}

:root {
	--wht: #fff;

	--color-primary: #368f90;
	--color-primary-light: #aad0d9;
	--color-primary-lightest: #d1e5e8;
	--color-grey: #2c2c2c;

	--font-s-1: 1rem;
	--font-s-2: 1.25rem;
	--font-s-3: 1.563rem;
	--font-s-4: 1.953rem;
	--font-s-5: 2.441rem;
	--font-s-6: 3.053rem;
	--font-s-7: 3.85rem;
	--font-s-8: 4.76rem;
	--font-s-9: 5.75rem;
	--font-s-10: 7rem;
}
</style>
