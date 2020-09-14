<template>
	<v-app>
		<v-app-bar app flat dense color="white">
			<v-row class="text-center">
				<v-col class="text-center">
					<Social />
				</v-col>
			</v-row>
		</v-app-bar>
		<router-view ></router-view>
	</v-app>
</template>

<script>
import Social from "@/components/Social.vue"
	export default {
		name: "App",
		components: {
			Social
		},
		data: () => ({
			//
		})
	};
</script>
<style>
	section {
		min-height: 100vh;
	}

	.navigator,
	.navigator-icon {
		-webkit-transition: -webkit-transform 0.6s ease-in-out;
		transition: transform 0.6s ease-in-out, color 2s;
	}
	.navigator-icon:hover {
		-webkit-transform: rotate(360deg) scale(1.5);
		transform: rotate(360deg) scale(1.5);
	}
	.navigator:hover {
		-webkit-transform: scale(1.3);
		transform: scale(1.3);
	}
</style>