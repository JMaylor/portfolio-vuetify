<template>
	<section id="projects">
		<div class="py-12"></div>

		<v-container>
			<h2
				class="display-2 font-weight-bold mb-3 text-uppercase text-center teal--text text--darken-2"
			>Projects</h2>

			<v-responsive class="mx-auto mb-12" width="56">
				<v-divider class="mb-1"></v-divider>

				<v-divider></v-divider>
			</v-responsive>

			<v-row>
				<v-col
					v-for="({ images, text, title, backEnd, frontEnd }, i) in articles"
					:key="i"
					cols="12"
					md="6"
				>
					<v-carousel height="auto">
						<v-carousel-item eager v-for="(image, j) in images" :key="j">
							<v-img eager :src="image"></v-img>
						</v-carousel-item>
					</v-carousel>

					<v-container>
						<v-row>
							<a :href="frontEnd.live" target="_blank" class="text-decoration-none teal--text">
								<h3 class="font-weight-black mb-4 text-uppercase" v-text="title"></h3>
							</a>
						</v-row>

						<v-row>
							<span class="title font-weight-light mb-5" v-html="text"></span>
						</v-row>

						<v-row>
							<a class="text-decoration-none" :href="frontEnd.repo" target="_blank">
								<v-chip class="ma-2" color="purple lighten-2" text-color="white">
									<v-avatar left>
										<v-icon>mdi-github</v-icon>
									</v-avatar>Front End
								</v-chip>
							</a>
							<a class="text-decoration-none" :href="backEnd.repo || backEnd.external" target="_blank">
								<v-chip
									class="ma-2"
									:color="backEnd.repo ? 'purple lighten-2' : 'teal' "
									text-color="white"
								>
									<v-avatar left>
										<v-icon>{{ backEnd.repo ? 'mdi-github' : 'mdi-web' }}</v-icon>
									</v-avatar>Back End
								</v-chip>
							</a>
							<a class="text-decoration-none" :href="frontEnd.live" target="_blank">
								<v-chip class="ma-2" color="red darken-4" text-color="white">
									<v-avatar left>
										<v-icon>mdi-star-outline</v-icon>
									</v-avatar>View Live
								</v-chip>
							</a>
							<a v-if="backEnd.db" class="text-decoration-none" :href="backEnd.db" target="_blank">
								<v-chip class="ma-2" color="primary accent-1" text-color="white">
									<v-avatar left>
										<v-icon>mdi-database</v-icon>
									</v-avatar>Database Diagram
								</v-chip>
							</a>
							<a v-if="frontEnd.alternate" class="text-decoration-none" :href="frontEnd.alternate" target="_blank">
								<v-chip class="ma-2" color="deep-orange accent-1" text-color="white">
									<v-avatar left>
										<v-icon>mdi-star-outline</v-icon>
									</v-avatar>In progress - New Front End Site
								</v-chip>
							</a>
						</v-row>
					</v-container>
					<v-divider />
				</v-col>
			</v-row>
			<v-row class="justify-center mb-2">
				<v-btn class="navigator" fab outlined @click="$vuetify.goTo('#cv')">
					<v-icon class="navigator-icon">mdi-chevron-double-up</v-icon>
				</v-btn>
			</v-row>
			<v-row class="justify-center">
				<v-btn class="navigator" fab outlined @click="$vuetify.goTo('#courses')">
					<v-icon class="navigator-icon">mdi-chevron-double-down</v-icon>
				</v-btn>
			</v-row>
		</v-container>
	</section>
</template>

<script>
	export default {
		data() {
			return {
				articles: [
					{
						images: [
							require("@/assets/walkies-1.png"),
							require("@/assets/walkies-2.png"),
							require("@/assets/walkies-3.png"),
							require("@/assets/walkies-4.png"),
							require("@/assets/walkies-5.png"),
							require("@/assets/walkies-6.png")
						],
						title: "Walkies",
						text:
							"I built a website for dog owners who sometimes want some human company while they walk their pets. A <b>RESTful API</b> built with <b>Python</b>/Flask performs <b>geoqueries</b> with location data in <b>MongoDB</b>, allowing you to find other users nearby, and arrange to meet up with them. The front end is built with <b>VueJS, Vuex and Vue Router</b>.",
						fatechs: ["mdi-vuejs"],
						backEnd: {
							repo: "https://github.com/JMaylor/walkies-backend",
							db: 'https://dbdiagram.io/d/5f3d0d59cf48a141ff556e74'
						},
						frontEnd: {
							repo: "https://github.com/JMaylor/walkies-vuetify",
							live: "https://walkies.maylor.io"
						}
					},
					{
						images: [
							require("@/assets/pokedex-1.png"),
							require("@/assets/pokedex-2.png")
						],
						title: "Pokedex",
						text:
							"Utilising an external API, I built a pokedex with <b>VueJS</b>. It allows you to search for pokemon, view their stats, see their evolution chain and add them to your favourites, which persists in <b>localStorage</b>.",
						backEnd: {
							external: "https://pokeapi.co"
						},
						frontEnd: {
							repo: "https://github.com/JMaylor/pokedex",
							live: "https://pokedex.maylor.io"
						}
					},
					{
						images: [
							require("@/assets/weather-1.png"),
							require("@/assets/weather-2.png"),
							require("@/assets/weather-3.png")
						],
						title: "Weather",
						text:
							"Utilising an external API, I built a weather app with <b>VueJS</b>. The site will automatically ask for access to your location and pass this information to the API.",
						backEnd: {
							external: "https://weatherapi.com"
						},
						frontEnd: {
							repo: "https://github.com/JMaylor/vue-weather-app",
							live: "https://weather.maylor.io"
						}
					},
					{
						images: [
							require("@/assets/todos-1.png"),
							require("@/assets/todos-2.png"),
							require("@/assets/todos-3.png")
						],
						title: "Todos",
						text:
							"A <b>CRUD</b> app with user authentication, built with <b>VueJS</b> and <b>Vuetify</b>.",
						backEnd: {
							repo: "https://github.com/JMaylor/task-manager-api"
						},
						frontEnd: {
							repo: "https://github.com/JMaylor/todos",
							live: "https://todos.maylor.io"
						}
					}
				]
			};
		},
	};
</script>