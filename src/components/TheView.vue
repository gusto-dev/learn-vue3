<template>
	<main>
		<div class="container py-4">
			<MyButton @click="sayHello" id="my-button" class="my-button"></MyButton>
		</div>
	</main>
</template>

<script>
import MyButton from '@/components/MyButton.vue';

export default {
	components: {
		MyButton,
	},
	setup() {
		const sayHello = () => {
			alert('Hello');
		};

		return {
			sayHello,
		};
	},
};
</script>

<style lang="scss" scoped></style>
