<template>
	<v-container>
		<v-main class="pt-0">
			<Hero />
			<Intro />
			<CV />
			<Projects />
			<v-row class="text-center">
				<v-col class="text-center">
					<Social />
				</v-col>
			</v-row>
		</v-main>
	</v-container>
</template>

<script>
	import Hero from "@/components/Hero";
	import Intro from "@/components/Intro";
	import CV from "@/components/CV";
	import Projects from "@/components/Projects";
	import Social from "@/components/Social"
	export default {
		components: {
			Hero,
			Intro,
			CV,
			Projects,
			Social
		},
		data() {
			return {};
		}
	};
</script>
