<template>
	<section id="hero">
		<v-row>
			<v-img
				:min-height="'calc(100vh - ' + $vuetify.application.top + 'px)'"
				src="https://images.unsplash.com/photo-1550645612-83f5d594b671?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80"
			>
				<v-theme-provider dark>
					<v-container fill-height fill-width>
						<v-row align="center" class="mx-auto" justify="center">
							<v-col class="white--text text-center py-0" cols="12">
								<span
									:class="[$vuetify.breakpoint.smAndDown ? 'display-1' : 'display-2']"
									class="font-weight-dark"
								>JOSEPH</span>
							</v-col>
							<v-col class="white--text text-center py-0" cols="12">
								<span
									:class="[$vuetify.breakpoint.smAndDown ? 'display-3': 'display-4']"
									class="font-weight-light"
								>MAYLOR</span>
							</v-col>
							<!-- <v-col class="text-center pt-0" cols="12">
								<Social />
							</v-col> -->

							<v-col class="white--text text-center" cols="12">
								<v-btn class="navigator" fab outlined @click="$vuetify.goTo('#intro')">
									<v-icon class="navigator-icon">mdi-chevron-double-down</v-icon>
								</v-btn>
							</v-col>
						</v-row>
					</v-container>
				</v-theme-provider>
			</v-img>
		</v-row>
	</section>
</template>

<script>
// import Social from "@/components/Social"
export default {
	components: {
		// Social
	}
}
</script>

<style scoped>
	.container {
		background: rgba(0, 0, 0, 0.7);
	}
</style>