<!-- TOGGLE -->
<template>
	<div>
		<vue-scroll-progress-bar
			height="0.3rem"
			zIndex="999"
			backgroundColor="linear-gradient(to right, var(--white-color), var(--white-color))"
		/>
		<div class="container">
			<input @change="toggleTheme" id="checkbox" type="checkbox" class="switch-checkbox" zIndex="999" />
			<label for="checkbox" class="switch-label">
				<span>🌙</span>
				<span>☀️</span>
				<div class="switch-toggle" :class="{ 'switch-toggle-checked': userTheme === 'dark-theme' }"></div>
			</label>
		</div>
	</div>
</template>

<script>
import { VueScrollProgressBar } from "@guillaumebriday/vue-scroll-progress-bar";

export default {
	name: "Toggle",
	components: {
		VueScrollProgressBar,
	},
	mounted() {
		const initUserTheme = this.getMediaPreference();
		this.setTheme(initUserTheme);
	},
	data() {
		return {
			userTheme: "light-theme",
		};
	},
	methods: {
		toggleTheme() {
			const activeTheme = localStorage.getItem("user-theme");
			if (activeTheme === "light-theme") {
				this.setTheme("dark-theme");
			} else {
				this.setTheme("light-theme");
			}
		},
		setTheme(theme) {
			localStorage.setItem("user-theme", theme);
			this.userTheme = theme;
			document.documentElement.className = theme;
		},
		getMediaPreference() {
			const hasDarkPreference = window.matchMedia(
				"(prefers-color-scheme: light)"
			).matches;
			if (hasDarkPreference) {
				return "dark-theme";
			} else {
				return "light-theme";
			}
		},
	},
};
</script>

<style scoped>
@import "../Toggle/Toggle.style.scss"
</style>
