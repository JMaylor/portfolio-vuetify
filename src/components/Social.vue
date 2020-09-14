<template>
	<span>
		<a
			v-for="({link, icon}, i) in socials"
			:key="i"
			:href="link"
			target="_blank"
			class="text-decoration-none"
		>
			<v-icon class="px-2">{{ icon }}</v-icon>
		</a>
	</span>
</template>

<script>
	export default {
		data() {
			return {
				socials: [
					{
						link: "mailto: joseph.maylor@gmail.com",
						icon: "mdi-email-outline"
					},
					{
						link: "tel:+447531613550",
						icon: "mdi-cellphone"
					},
					{
						link: "https://stackoverflow.com/users/4981786/maylor?tab=answers",
						icon: "mdi-stack-overflow"
					},
					{
						link: "https://github.com/JMaylor",
						icon: "mdi-github"
					},
					{
						link: "https://www.linkedin.com/in/joe-maylor-547399a7/",
						icon: "mdi-linkedin"
					},
					{
						link: "https://docs.google.com/document/d/1VMJeoFwGZRVdtvVE5DIxDz7ffLdfMTlYcVx5BXuMCwI/edit?usp=sharing",
						icon: "mdi-school-outline"
					}
				]
			};
		}
	};
</script>

<style scoped>
	.mdi-stack-overflow {
		color: #f48024 !important;
	}

	.mdi-github {
		color: #6e5494 !important;
	}

	.mdi-linkedin {
		color: #0077b5 !important;
	}

	.mdi-school-outline {
		color: rgb(3, 124, 3) !important;
	}

	.mdi-email-outline {
		color: rgb(168, 175, 41) !important;
	}

	.mdi-cellphone {
		color: rgb(204, 54, 54) !important;
	}

	[class*="mdi"] {
		-webkit-transition: -webkit-transform 2s ease-in-out;
		transition: transform 2s ease-in-out, color 2s;
	}

	[class*="mdi"]:hover {
		-webkit-transform: scale(1.5);
		transform: scale(1.5);
	}
</style>