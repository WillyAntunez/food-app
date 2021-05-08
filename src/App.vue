<template>
	<div id="app">
		<div class="navbar-container">
			<div class="navbar-content">
				<RouterLink to="/">
					<i class="bx bx-home-alt bx-sm"></i>
				</RouterLink>
				<RouterLink to="/cesta">
					<i class="bx bx-message-square-detail bx-sm"></i>
				</RouterLink>
				<RouterLink to="/favoritos">
					<i class="bx bx-heart bx-sm"></i>
				</RouterLink>
				<RouterLink to="/historial">
					<i class="bx bx-alarm-exclamation bx-sm"></i>
				</RouterLink>
			</div>
		</div>
		<router-view />
	</div>
</template>

<style lang="less">
.navbar-container {
	width: 100%;
	position: fixed;
	bottom: 0px;
	.navbar-content {
		padding: 10px;
		display: flex;
		justify-content: space-between;
		a {
			padding: 20px;
			color: rgba(163, 163, 163);
		}
		.router-link-exact-active {
			color: rgba(255, 131, 62);
		}
	}
}

* {
	font-family: 'josefin Sans', sans-serif;
	margin: 0px;
	padding: 0px;
}

#app {
	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	color: #2c3e50;
}

#nav {
	padding: 30px;

	a {
		font-weight: bold;
		color: #2c3e50;
	}
}
</style>
