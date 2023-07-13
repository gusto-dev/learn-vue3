<template>
	<div class="p-3 bg-danger">
		<button class="btn btn-primary" type="button" v-bind="$attrs">
			My Button
		</button>
		<!-- {{$attrs}} -->
	</div>
</template>

<script>
export default {
	inheritAttrs: false,
	setup(props, { attrs }) {
		console.log(attrs);
		// console.log(attrs.class);
		// console.log(attrs.onClick);
		// attrs.onClick();
		return {};
	},
};
</script>

<style lang="scss" scoped></style>
