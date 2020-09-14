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
					<v-carousel cycle height="auto" show-arrows-on-hover>
						<v-carousel-item v-for="(image, j) in images" :key="j">
							<v-img :src="image"></v-img>
						</v-carousel-item>
					</v-carousel>

					<v-container>
						<v-row>
							<a :href="frontEnd.live" target="_blank" class="text-decoration-none teal--text"><h3 class="font-weight-black mb-4 text-uppercase" v-text="title"></h3></a>
						</v-row>

						<v-row>
							<span class="title font-weight-light mb-5" v-text="text"></span>
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
						</v-row>
					</v-container>
					<v-divider />
				</v-col>
			</v-row>
			<v-row class="justify-center">
				<v-btn class="navigator" fab outlined @click="$vuetify.goTo('#cv')">
					<v-icon class="navigator-icon">mdi-chevron-double-up</v-icon>
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
							"https://d33wubrfki0l68.cloudfront.net/5f5d00a407291a0008104b3d/screenshot.png"
						],
						title: "Walkies",
						text:
							"I built a website for dog owners who sometimes want some human company while they walk their pets. A RESTful API built with Python/Flask performs geoqueries with location data in MongoDB, allowing you to find other users nearby, and arrange to meet up with them. The front end is built with VueJS, Vuex and Vue Router.",
						backEnd: {
							techs: ["Python", "Flask", "MongoDB"],
							repo: "https://github.com/JMaylor/walkies-backend"
						},
						frontEnd: {
							techs: ["mdi-vuejs", "mdi-bootstrap"],
							repo: "https://github.com/JMaylor/walkies-frontend",
							live: "https://walkies.maylor.io"
						}
					},
					{
						images: [
							"https://d33wubrfki0l68.cloudfront.net/5f5d060af1a4de0007c6c74b/screenshot.png"
						],
						title: "Pokedex",
						text:
							"Nam ut leo ipsum. Maecenas pretium aliquam feugiat. Aenean vel tempor est, vitae tincidunt risus. Sed sodales vestibulum nibh.",
						backEnd: {
							external: "https://pokeapi.co"
						},
						frontEnd: {
							techs: ["mdi-vuejs", "mdi-bootstrap"],
							repo: "https://github.com/JMaylor/pokedex",
							live: "https://pokedex.maylor.io"
						}
					},
					{
						images: [
							"https://d33wubrfki0l68.cloudfront.net/5f5940c3ca644e00071c867f/screenshot.png"
						],
						title: "Weather",
						text:
							"Vestibulum in dictum velit, in rhoncus nibh. Maecenas neque libero, interdum a dignissim in, aliquet vitae lectus. Phasellus lorem enim, luctus ut velit eget.",
						backEnd: {
							external: "https://weatherapi.com"
						},
						frontEnd: {
							techs: ["mdi-vuejs"],
							repo: "https://github.com/JMaylor/vue-weather-app",
							live: "https://weather.maylor.io"
						}
					},
					{
						images: [
							"https://d33wubrfki0l68.cloudfront.net/5f5e4ca8804897000899f94d/screenshot.png"
						],
						title: "Todos",
						text:
							"Vestibulum in dictum velit, in rhoncus nibh. Maecenas neque libero, interdum a dignissim in, aliquet vitae lectus. Phasellus lorem enim, luctus ut velit eget.",
						backEnd: {
							techs: ["Python", "Flask", "MongoDB"],
							repo: "https://github.com/JMaylor/task-manager-api"
						},
						frontEnd: {
							techs: ["mdi-vuejs", "mdi-vuetify"],
							repo: "https://github.com/JMaylor/todos",
							live: "https://todos.maylor.io"
						}
					}
				]
			};
		}
	};
</script>