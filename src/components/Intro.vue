<template>
	<section id="intro">

		<v-container class="text-center">
			<h2 class="display-2 font-weight-bold mb-3 teal--text text--darken-2">Intro</h2>

			<v-responsive class="mx-auto mb-8" width="56">
				<v-divider class="mb-1"></v-divider>

				<v-divider></v-divider>
			</v-responsive>

			<v-responsive class="mx-auto title font-weight-light mb-8" max-width="720">
				My name's Joe, I'm a 26 year-old self-taught programmer. I've been working as a currency trader and execution analyst for the past five years, since graduating.
				<br />
				<br />I started learning code initially for fun, and I'm now hooked and looking to make it something I do full time.
				<br />
				<br /> I used MatLab and Java at university, and since graduating I've worked extensively with VBA at work, and self-taught Python, HTML, CSS and JavaScript.
			</v-responsive>

			<v-avatar class="elevation-6 mb-12" size="128">
				<span class="teal--text display-3">JM</span>
			</v-avatar>

			<div></div>
			<v-row class="justify-center mb-2">
				<v-btn class="navigator" fab outlined @click="$vuetify.goTo('#hero')">
					<v-icon class="navigator-icon">mdi-chevron-double-up</v-icon>
				</v-btn>
			</v-row>

			<v-row class="justify-center">
				<v-btn class="navigator" fab outlined @click="$vuetify.goTo('#cv')">
					<v-icon class="navigator-icon">mdi-chevron-double-down</v-icon>
				</v-btn>
			</v-row>
		</v-container>

		<div class="py-12"></div>
	</section>
</template>