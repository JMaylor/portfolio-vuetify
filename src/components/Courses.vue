<template>
	<section id="courses" class="grey lighten-3">
		<div class="py-12"></div>

		<v-container>
			<h2 class="display-2 font-weight-bold mb-3 teal--text text--darken-2 text-center">COURSES</h2>

			<v-responsive class="mx-auto" width="56">
				<v-divider class="mb-1"></v-divider>

				<v-divider></v-divider>
			</v-responsive>

			<v-row>
				<v-col v-for="(course, i) in courses" :key="i" cols="12" md="6">
					<Course :course="course" />
				</v-col>
			</v-row>
			<v-row class="justify-center mb-2">
				<v-btn class="navigator" fab outlined @click="$vuetify.goTo('#projects')">
					<v-icon class="navigator-icon">mdi-chevron-double-up</v-icon>
				</v-btn>
			</v-row>
		</v-container>
	</section>
</template>

<script>
	import Course from "@/components/Course";
	export default {
		components: {
			Course
		},
		data() {
			return {
				courses: [
					{
						img:
							"https://upload.wikimedia.org/wikipedia/commons/1/10/CSS3_and_HTML5_logos_and_wordmarks.svg",
						title: "Response Web Design - HTML5 & CSS3",
						link:
							"https://www.udemy.com/course/responsive-web-design-tutorial-course-html5-css3-bootstrap/",
						author: "Daniel Walter Scott",
						descriptions: [
							"Learn how to work with responsive images and icons. and stunning full screen background images and probably one too many gradients.",
							"Learn how to work with Bootstrap 4 to easily add carousels, cards and complex looking menus.",
							"Learn how to create forms and to choose great fonts for your website.",
							"Setup a domain name with hosting so that your website is live on the internet for others to see."
						]
					},
					{
						img:
							"https://preview.redd.it/fi0fu2k24eo31.png?width=720&format=png&auto=webp&s=d88fd59e0924e11728c01be84fab0d55b9f4a81a",
						title: "The Complete JavaScript Course",
						link:
							"https://www.udemy.com/course/the-complete-javascript-course/",
						author: "Jonas Schmedtmann",
						descriptions: [
							"JavaScript and programming fundamentals: variables, boolean logic, if/else, loops, functions, arrays, etc.",
							"Asynchronous JavaScript: The event loop, promises, async/await, AJAX and APIs",
							"Complex features like the 'this' keyword, function constructors, prototypal inheritance, first-class functions, closures",
							"Modern JavaScript for 2020: NPM, Webpack, Babel and ES6 modules.",
							"What's new in ES6: arrow functions, classes, default and rest parameters, etc."
						]
					},
					{
						img:
							"https://nodejs.org/static/images/logos/nodejs-new-pantone-black.svg",
						title: "The Complete Node.js Developer Course",
						link:
							"https://www.udemy.com/course/the-complete-nodejs-developer-course-2/",
						author: "Andrew Mead",
						descriptions: [
							"Create Express web servers and APIs",
							"Use cutting-edge ES6/ES7 JavaScript",
							"Build, test, and launch Node apps",
							"Store data with Mongoose and MongoDB"
						]
					},
					{
						img: "https://vuejs.org/images/logo.png",
						title: "Vue JS - The Complete Guide",
						link:
							"https://www.udemy.com/course/vuejs-2-the-complete-guide/",
						author: "Maximilian Schwarzmüller",
						descriptions: [
							"Build amazing Vue.js Applications - all the Way from Small and Simple Ones up to Large Enterprise-level Ones",
							"Leverage Vue.js in both Multi- and Single-Page-Applications (MPAs and SPAs)",
							"Understand the Theory behind Vue.js and use it in Real Projects"
						]
					}
				],
				show: [false, false, false, false]
			};
		}
	};
</script>

<style scoped>
	section {
		min-height: 10vh;
	}
</style>