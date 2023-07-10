<template>
	<div>
		<nav class="navbar navbar-expand-sm navbar-dark bg-primary">
			<div class="container-fluid">
				<a class="navbar-brand" href="#">Navbar</a>
				<button
					class="navbar-toggler"
					type="button"
					data-bs-toggle="collapse"
					data-bs-target="#navbarSupportedContent"
					aria-controls="navbarSupportedContent"
					aria-expanded="false"
					aria-label="Toggle navigation"
				>
					<span class="navbar-toggler-icon"></span>
				</button>
				<div class="collapse navbar-collapse" id="navbarSupportedContent">
					<ul class="navbar-nav me-auto">
						<li class="nav-item">
							<a class="nav-link active" aria-current="page" href="#">Home</a>
						</li>
						<li class="nav-item">
							<a class="nav-link" href="#">Link</a>
						</li>
						<li class="nav-item dropdown">
							<a
								class="nav-link dropdown-toggle"
								href="#"
								role="button"
								data-bs-toggle="dropdown"
								aria-expanded="false"
							>
								Dropdown
							</a>
							<ul class="dropdown-menu">
								<li><a class="dropdown-item" href="#">Action</a></li>
								<li><a class="dropdown-item" href="#">Another action</a></li>
								<li><hr class="dropdown-divider" /></li>
								<li>
									<a class="dropdown-item" href="#">Something else here</a>
								</li>
							</ul>
						</li>
						<li class="nav-item">
							<a class="nav-link disabled">Disabled</a>
						</li>
					</ul>
					<form class="d-flex" role="search">
						<input
							class="form-control me-2"
							type="search"
							placeholder="Search"
							aria-label="Search"
						/>
						<button class="btn btn-outline-success" type="submit">
							Search
						</button>
					</form>
				</div>
			</div>
		</nav>
		<p class="text" :class="{ active: isActive }">{{ message }}</p>
		<button @click="toggle">toggle</button>
		<p v-once>{{ message }}</p>
		<button v-on:click="message = message + '!'">click</button>
	</div>
</template>

<script>
import { ref } from 'vue';

export default {
	setup() {
		const message = ref('안녕하세요');
		const isActive = ref(true);

		const toggle = () => {
			isActive.value = !isActive.value;
		};

		return {
			message,
			isActive,
			toggle,
		};
	},
};
</script>

<style scoped>
.active {
	color: red;
}
</style>
