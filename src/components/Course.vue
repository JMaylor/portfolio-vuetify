<template>
	<v-card class="mx-auto" color="grey lighten-5" shaped ripple>
		<a :href="course.link" target="_blank" class="text-decoration-none teal--text">
			<v-card-title>{{ course.title }}</v-card-title>
		</a>
		<a :href="course.link" target="_blank">
			<v-img :src="course.img" height="200px" contain></v-img>
		</a>

		<v-card-subtitle>{{ course.author }}</v-card-subtitle>

		<v-card-actions>
			<v-btn icon @click="show = !show">
				<v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
			</v-btn>
		</v-card-actions>

		<v-expand-transition>
			<div v-show="show">
				<v-divider></v-divider>

				<v-card-text>
					<ul>
						<li v-for="(description, i) in course.descriptions" :key="i">
							{{description}}
						</li>
					</ul>
				</v-card-text>
			</div>
		</v-expand-transition>
	</v-card>
</template>

<script>
	export default {
		props: ["course"],
		data() {
			return {
				show: false
			};
		}
	};
</script>