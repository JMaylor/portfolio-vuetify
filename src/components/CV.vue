<template>
	<section id="cv" class="grey lighten-3">
		<div class="py-12"></div>

		<v-container class="text-center">
			<h2 class="display-2 font-weight-bold mb-3 teal--text text--darken-2">CV</h2>

			<v-responsive class="mx-auto" width="56">
				<v-divider class="mb-1"></v-divider>

				<v-divider></v-divider>
			</v-responsive>
			<v-row mb-12>
				<v-col class="text-center">
					<a
						class="text-decoration-none"
						href="https://docs.google.com/document/d/1VMJeoFwGZRVdtvVE5DIxDz7ffLdfMTlYcVx5BXuMCwI/edit?usp=sharing"
						target="_blank"
					>
						<v-chip class="ma-2" color="orange lighten-2" text-color="white">
							<v-avatar left>
								<v-icon>mdi-school-outline</v-icon>
							</v-avatar>View on Google Docs
						</v-chip>
					</a>
				</v-col>
			</v-row>
			<v-responsive class="mx-auto" width="56">
				<v-divider class="mb-1"></v-divider>

				<v-divider></v-divider>
			</v-responsive>

			<v-row>
				<v-col v-for="({ icon, title, text }, i) in features" :key="i" cols="12" md="4">
					<v-card class="py-12 px-4" color="grey lighten-5" flat>
						<v-theme-provider dark>
							<div>
								<v-avatar color="teal darken-4" size="88">
									<v-icon large v-text="icon"></v-icon>
								</v-avatar>
							</div>
						</v-theme-provider>

						<v-card-title class="justify-center font-weight-black text-uppercase" v-text="title"></v-card-title>

						<v-card-text class="subtitle-1" v-text="text"></v-card-text>
					</v-card>
				</v-col>
			</v-row>
			<v-row class="justify-center mb-2">
				<v-btn class="navigator" fab outlined @click="$vuetify.goTo('#intro')">
					<v-icon class="navigator-icon">mdi-chevron-double-up</v-icon>
				</v-btn>
			</v-row>
			<v-row class="justify-center">
				<v-btn class="align-self-end navigator" fab outlined @click="$vuetify.goTo('#projects')">
					<v-icon class="navigator-icon">mdi-chevron-double-down</v-icon>
				</v-btn>
			</v-row>
		</v-container>

		<div class="py-12"></div>
	</section>
</template>

<script>
	export default {
		data() {
			return {
				features: [
					{
						icon: "mdi-school-outline",
						title: "Education",
						text:
							"High achiever, with a 1st in Maths from the University of Warwick, and three A*s at A-Level in Maths, Further Maths and Economics."
					},
					{
						icon: "mdi-briefcase-outline",
						title: "Employment",
						text:
							"Five years of experience in Foreign Exchange trading. Promoted from entry level analyst to Associate Director in four years."
					},
					{
						icon: "mdi-certificate",
						title: "Courses",
						text:
							"Have taken Udemy courses on HTML, CSS, JavaScript, NodeJS and VueJS. Details of these courses can be found below."
					}
				]
			};
		}
	};
</script>

<style>
	.v-chip:hover {
		cursor: pointer;
	}
</style>