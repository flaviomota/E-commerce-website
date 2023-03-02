<template>
	<nav>
		<div class="nav-inner">
			<!-- Logo -->
			<div class="logo">
				<img src="@/assets/images/logo.png" alt="Shop Logo"/>
			</div>
			<!-- Links -->
			<div class="links">
				<a href="#">About Us</a>
				<a href="#">Women</a>
				<a href="#">Men</a>
				<a href="#">Beauty</a>
				<a href="#">Accessories</a>
				<a href="#">Blog</a>
				<a href="#">Contact</a>
			</div>
			<!-- Icons -->
			<div class="icons">
				<span class="icon">
					<img src="@/assets/images/lupa.png" alt=""/>
				</span>
				<span class="icon">
					<img src="@/assets/images/worldwide.png" alt=""/>
				</span>
				<span class="icon">
					<img src="@/assets/images/user.png" alt=""/>
				</span>
				<span class="icon">
					<img src="@/assets/images/bag.png" alt=""/>
				</span>
			</div>
		</div>
	</nav>
</template>

<script setup>

</script>

<style lang="scss" scoped>
nav {
	border-bottom: 2px solid #f8f8f8;
}
nav .nav-inner {
	//background-color: red;
	height: 90px;
	display: flex;
	justify-content: space-between;
	align-items: center;
	max-width: calc(1440px - 170px);
	widows: 100%;
	margin: auto;
}

.nav-inner .links a {
	margin: 0px 16px;
	font-style: normal;
	font-weight: 400;
	font-size: 16px;
	line-height: 1.25;
	color: #121212;
	border-bottom:  1px solid transparent;
	transition:  0.3s;
}

.nav-inner .links a:hover {
	border-color: #121212;
}

.icon img {
	width: 20px;
	height: 20px;
}

.icons {
	display: flex;
	align-items: center;
}

.icons span {
	margin: 0 13px;
	display: flex;
	justify-content: center;
	align-items: center;
}
</style>