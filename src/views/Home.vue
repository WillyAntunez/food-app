<template>
	<div class="home">
		<div class="header">
			<h2 class="title">Hi <b>Vadim!</b></h2>
			<div class="input">
				<input type="text" placeholder="Find what you want..." />
				<div class="icon-input">
					<i class="bx bx-search"></i>
				</div>
			</div>

			<div class="combo-header">
				<div class="text">
					<h3><b>Free combo</b></h3>
					<p>Burguer + Coca Cola for new users</p>
				</div>
				<div class="img">
					<img
						src="https://images.unsplash.com/photo-1513104890138-7c749659a591?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=750&q=80"
						alt="pizza"
					/>
				</div>
			</div>
		</div>

		<div class="scroll-menu">
			<div class="scroll-content">
				<div class="avatar" v-for="(item, index) in 10" :key="index">
					<i class="bx bxs-pizza bx-sm"></i>
				</div>
			</div>
		</div>

		<h2><b>Top products</b></h2>
		<div class="scroll-menu">
			<div class="scroll-content">
				<div class="top-products" v-for="(item, index) in 10" :key="index">
					<div class="top-products-img">
						<img
							src="https://images.unsplash.com/photo-1547584370-2cc98b8b8dc8?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1051&q=80"
							alt="Hamburguer"
						/>
					</div>

					<div class="top-products-text">
						<div class="top-products-title"><b>Berry Juice</b></div>
						<div class="top-products-price">$7.5</div>
					</div>

					<i class="bx bx-plus-medical"></i>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: 'Home',
	components: {},
};
</script>

<style lang="less">
.home {
	margin: 20px;
}

.top-products {
	background-color: rgb(236, 236, 236);
	padding: 10px;
	position: relative;
	min-width: 150px;
	border-radius: 10px;
	margin: 5px;
	.top-products-img {
		img {
			width: 100%;
		}
	}
	.top-products-text {
		margin-top: 10px;
		.top-product-title {
			color: rgba(47, 47, 47);
		}
		.top-products-price {
			color: rgba(255, 131, 62);
		}
	}
	i {
		background-color: rgba(74, 174, 84);
		padding: 10px;
		color: white;
		border-radius: 50px;
		position: absolute;
		right: 0px;
		bottom: 0px;
		margin: 5px;
	}
}

.scroll-menu {
	margin-top: 10px;
	.scroll-content {
		display: flex;
		overflow-y: auto;
		.avatar {
			background-color: rgba(250, 248, 248);
			padding: 20px;
			border-radius: 10px;
			margin: 5px;
			i {
				color: rgba(255, 131, 62);
			}
		}
	}
}

.header {
	.input {
		display: flex;
		position: relative;
		align-items: center;
		margin-top: 10px;
		input {
			width: 100%;
			background-color: rgba(250, 248, 248);
			border: 0px;
			outline: none;
			padding: 10px;
			border-radius: 10px;
			padding-left: 30px;
		}
		.icon-input {
			position: absolute;
			margin-left: 10px;
		}
	}
	.title {
		font-weight: 350;
	}

	.combo-header {
		background-color: rgba(74, 174, 84);
		color: white;
		padding: 20px;
		border-radius: 20px;
		display: flex;
		justify-content: space-between;
		align-items: center;
		margin-top: 20px;
		.text {
			width: 50%;
			h3 {
				font-weight: 500;
			}
			p {
				font-weight: 300;
			}
		}
		.img {
			width: 50%;
			object-fit: cover;
			img {
				width: 100%;
			}
		}
	}
}
</style>
