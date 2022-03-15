<template>
	<transition name="fade">
		<div class="modal" v-if="show">
			<div class="modal__backdrop" @click="closeModal()" />
			<div class="modal__dialog">
				<div class="modal__header">
					<slot name="header" />
				</div>
				<div class="modal__body">
					<slot name="body" />
				</div>
			</div>
		</div>
	</transition>
</template>

<script>
export default {
	name: "Modal",
	data() {
		return {
			show: false,
		};
	},
	methods: {
		closeModal() {
			this.show = false;
			document.querySelector("body").classList.remove("overflow-hidden");
		},
		openModal() {
			this.show = true;
			document.querySelector("body").classList.add("overflow-hidden");
		},
	},
};
</script>

<style lang="scss" scoped>
@import "../../style.scss";
@import "../../style.breakpoints.scss";
@import "../Modal/Modal.style.scss";
</style>
