<template>
	<section id="cv" class="grey lighten-3">
		<div class="py-12"></div>

		<v-container class="text-center">
			<h2
				class="display-2 font-weight-bold mb-3 teal--text text--darken-2"
			>
				CV
			</h2>

			<v-responsive class="mx-auto" width="56">
				<v-divider class="mb-1"></v-divider>

				<v-divider></v-divider>
			</v-responsive>
			<v-row mb-12>
				<v-col class="text-center">
					<a
						class="text-decoration-none"
						href="https://docs.google.com/document/d/15uINqDliusAEY3P7R-O6oCL00XmY95WvGDgCwH1TlFI/edit?usp=sharing"
						target="_blank"
					>
						<v-chip
							class="ma-2"
							color="orange lighten-2"
							text-color="white"
						>
							<v-avatar left>
								<v-icon>mdi-school-outline</v-icon> </v-avatar
							>View on Google Docs
						</v-chip> </a
					><br />
					<a
						class="text-decoration-none"
						:href="`${publicPath}Joseph Maylor CV.pdf`"
						download
					>
						<v-chip
							class="ma-2"
							color="teal lighten-2"
							text-color="white"
						>
							<v-avatar left>
								<v-icon>mdi-file-pdf</v-icon> </v-avatar
							>Download as PDF
						</v-chip>
					</a>
				</v-col>
			</v-row>
			<v-responsive class="mx-auto" width="56">
				<v-divider class="mb-1"></v-divider>

				<v-divider></v-divider>
			</v-responsive>

			<v-row>
				<v-col
					v-for="({ icon, title, text }, i) in features"
					:key="i"
					cols="12"
					md="4"
				>
					<v-card class="py-12 px-4" color="grey lighten-5" flat>
						<v-theme-provider dark>
							<div>
								<v-avatar color="teal darken-4" size="88">
									<v-icon large v-text="icon"></v-icon>
								</v-avatar>
							</div>
						</v-theme-provider>

						<v-card-title
							class="justify-center font-weight-black text-uppercase"
							v-text="title"
						></v-card-title>

						<v-card-text
							class="subtitle-1"
							v-html="text"
						></v-card-text>
					</v-card>
				</v-col>
			</v-row>
			<v-row class="justify-center mb-2">
				<v-btn
					class="navigator"
					fab
					outlined
					@click="$vuetify.goTo('#intro')"
				>
					<v-icon class="navigator-icon"
						>mdi-chevron-double-up</v-icon
					>
				</v-btn>
			</v-row>
			<v-row class="justify-center">
				<v-btn
					class="align-self-end navigator"
					fab
					outlined
					@click="$vuetify.goTo('#projects')"
				>
					<v-icon class="navigator-icon"
						>mdi-chevron-double-down</v-icon
					>
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
				publicPath: process.env.BASE_URL,
				features: [
					{
						icon: "mdi-school-outline",
						title: "Education",
						text:
							"High achiever, with a <b>1st</b> in <b>Maths</b> from the University of <b>Warwick</b>, and three A*s at A-Level in Maths, Further Maths and Economics."
					},
					{
						icon: "mdi-briefcase-outline",
						title: "Employment",
						text:
							"Five years of experience in Foreign Exchange trading. Promoted from entry level analyst to <b>Associate Director</b> in four years."
					},
					{
						icon: "mdi-certificate",
						title: "Courses",
						text:
							"Have taken Udemy courses on <b>HTML</b>, CSS, <b>JavaScript</b>, NodeJS and VueJS, as well as free YouTube courses on <b>Python</b>, Flask and Django."
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